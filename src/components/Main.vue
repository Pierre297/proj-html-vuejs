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
      <div class="work-card">
        <RecentWork
          v-for="(work, secondkey) in works"
          :key="secondkey"
          :work="work"
        />
      </div>
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
      <b>HARRY SMITH &#8226; NEW HOME OWNER</b>
    </div>
    <!-- NEWS -->
    <div class="latest-news">
      <h3>Latest News</h3>
      <div class="line"></div>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Aspernatur
        minus eos neque, amet odit suscipit earum minima nisi aut enim beatae
        expedita officiis repudiandae atque, nulla vel dolorum molestiae nam?
      </p>
      <div class="news-container">
        <NewsCard
          v-for="(article, fourthkey) in articles"
          :key="fourthkey"
          :news="article"
        />
      </div>
    </div>
  </main>
</template>

<script>
import InfoCard from "./InfoCard.vue";
import RecentWork from "./RecentWork.vue";
import CoreValue from "./CoreValue.vue";
import NewsCard from "./NewsCard.vue";

export default {
  name: "Main",
  components: {
    InfoCard,
    RecentWork,
    CoreValue,
    NewsCard,
  },
  data() {
    return {
      infos: [
        {
          class: "fas fa-suitcase",
          number: "3534",
          role: "PLANNING APPLICATIONS",
        },
        {
          class: "far fa-building",
          number: "896",
          role: "COMPLETED PROJECTS",
        },
        {
          class: "fas fa-users",
          number: "172",
          role: "TRAINED PROFESSIONALS",
        },
        {
          class: "fas fa-globe",
          number: "19",
          role: "INTERNATIONALS OFFICES",
        },
      ],

      works: [
        {
          image: "project2-featured-15013609.jpg",
          title: "Florida Health Facility",
          role: "Commercial",
        },
        {
          image: "project1-featured-294276386.jpg",
          title: "Florida Health Facility",
          role: "Commercial",
        },
        {
          image: "project3-featured-189023420.jpg",
          title: "Florida Health Facility",
          role: "Commercial",
        },
      ],
      cores: [
        {
          color: "lightblue",
          class: "fas fa-home",
          title: "Great Services",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
        {
          color: "blue",
          class: "fas fa-cog",
          title: "Highest Standard",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
        {
          color: "orange",
          class: "fas fa-users",
          title: "Professional Team",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
        {
          color: "green",
          class: "far fa-lightbulb",
          title: "Creative Solutions",
          text: "Neque porro quisiquam est, qui dolorem ipsum quia dolor sit amet. consectetur, adipisci velid, seid quas",
        },
      ],
      articles: [
        {
          img: "blog-post-134132600.jpg",
          title: "Redeveloping Florida's Remote Southen Coast",
          date: "December 7th, 2015",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, quaerat ea enim itaque eaque obcaeca sit ut exercitationem minima fugiat cumque, deleniti similique? Aliquam deleniti",
        },
        {
          img: "blog-post-92486644.jpg",
          title: "How We Manage Large Construction Projects",
          date: "December 7th, 2015",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, quaerat ea enim itaque eaque obcaeca sit ut exercitationem minima fugiat cumque, deleniti similique? Aliquam deleniti",
        },
        {
          img: "blog-post-332773904.jpg",
          title: "Future Proofing a Modern Home",
          date: "December 6th, 2015",
          text: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium, quaerat ea enim itaque eaque obcaeca sit ut exercitationem minima fugiat cumque, deleniti similique? Aliquam deleniti",
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
.work-card {
  width: 60%;
  margin-left: 20%;
  height: 550px;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
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

// LATEST NEWS
.latest-news {
  background-color: #f5f5f5;
  height: 1000px;

  h3 {
    padding-top: 100px;
    font-size: 30px;
  }
  p {
    width: 40%;
    margin-left: 30%;
    line-height: 30px;
  }
}
.news-container {
  height: 550px;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>