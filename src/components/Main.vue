<template>
  <main>
    <!-- STATISTICS -->
    <div class="statistics-container">
      <InfoCard v-for="(info, i) in infos" :key="i" :info="info" />
    </div>
    <!-- RECENT WORK -->
    <div class="recent-work">
      <h3>Explore Recent Work</h3>
      <div class="line"></div>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aliquid
        doloribus aut, fugiat veniam quo id sequi magni et distinctio ipsum
        facilis quasi, vitae tenetur, minima iste? Nihil ab quisquam autem?
      </p>
      <!-- card -->
      <RecentWork
        v-for="(work, secondkey) in works"
        :key="secondkey"
        :work="work"
      />
    </div>
    <!-- CORE VALUES -->
    <div class="core-container">
      <h3>Our Core Values</h3>
      <div class="line"></div>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Magnam facilis
        officia doloremque. Laboriosam ut beatae atque accusantium dolor
        officia?
      </p>
      <!-- card -->
      <div class="value-container">
        <CoreValue
          v-for="(core, thirdkey) in cores"
          :key="thirdkey"
          :value="core"
        />
      </div>
    </div>
    <!-- REVIEW -->
    <div class="review-container">
      <h4>Our Home Owners Say</h4>
      <div class="line"></div>
      <img
        class="profile-picture"
        src="../assets/home-testimonial-113165296.jpg"
        alt="testimonial profile picture"
      />
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium,
        quaerat ea enim itaque eaque obcaecati sit ut exercitationem minima
        officiis cupiditate fugiat cumque, deleniti similique? Aliquam deleniti
        necessitatibus repudiandae at.
      </p>
      <b>HARRY SMITH NEW HOME OWNER</b>
    </div>
    <!-- NEWS -->
    <div></div>
  </main>
</template>

<script>
import InfoCard from "./InfoCard.vue";
import RecentWork from "./RecentWork.vue";
import CoreValue from "./CoreValue.vue";

export default {
  name: "Main",
  components: {
    InfoCard,
    RecentWork,
    CoreValue,
  },
  data() {
    return {
      infos: [
        {
          thumb: "",
          number: "3534",
          role: "PLANNING APPLICATIONS",
        },
        {
          thumb: "",
          number: "896",
          role: "COMPLETED PROJECTS",
        },
        {
          thumb: "",
          number: "172",
          role: "TRAINED PROFESSIONALS",
        },
        {
          thumb: "",
          number: "19",
          role: "INTERNATIONALS OFFICES",
        },
      ],

      works: [
        {
          image: "../assets/project2-featured-15013609.jpg",
          title: "Florida Health Facility",
          role: "Commercial",
        },
        {
          image: "../assets/project1-featured-294276386.jpg",
          title: "Florida Health Facility",
          role: "Commercial",
        },
        {
          image: "../assets/project3-featured-189023420.jpg",
          title: "Florida Health Facility",
          role: "Commercial",
        },
      ],
      cores: [
        {
          image: "",
          title: "Great Services",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
        {
          image: "",
          title: "Highest Standard",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
        {
          image: "",
          title: "Professional Team",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
        {
          image: "",
          title: "Creative Solutions",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
// <!-- STATISTICS -->
.statistics-container {
  margin-top: 60px;
  height: 550px;
  background-image: url("../assets/home-244125289.jpg");
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

// <!-- RECENT WORK -->
.recent-work {
  h3 {
    font-size: 35px;
    margin-top: 150px;
  }
  p {
    width: 40%;
    margin-left: 30%;
    line-height: 35px;
  }
}
.line {
  border: 1px solid #fed03d;
  margin: 60px 0px;
  width: 10%;
  margin-left: 45%;
}

// CORE VALUES
.core-container {
  background-color: #f5f5f5;
  h3 {
    margin-top: 150px;
    font-size: 30px;
    padding-top: 50px;
  }
  p {
    width: 40%;
    margin-left: 30%;
    line-height: 35px;
  }
}
.value-container {
  margin-top: 60px;
  height: 550px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

// REVIEW
.review-container {
  background-image: url("../assets/home-parallax-144609983.jpg");
  background-size: 1600px;
  height: 700px;

  h4 {
    color: white;
    padding-top: 100px;
    font-size: 30px;
  }
  p {
    color: white;
    margin-top: 60px;
    width: 40%;
    margin-left: 30%;
    line-height: 30px;
    margin-bottom: 50px;
  }
  b {
    font-size: 20px;
    color: white;
    margin-top: 60px;
    width: 40%;
  }
}

.profile-picture {
  border-radius: 50%;
}
</style>