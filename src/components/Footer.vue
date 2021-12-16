<template>
  <footer>
    <!-- PARTNERS -->
    <div class="partner-container">
      <h3>Trusted Partners</h3>
      <div class="line"></div>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi ut
        provident, incidunt ipsa quis dolorem quae vero, cumque reprehenderit
        expedita atque. Nisi error nobis ea voluptas eos ducimus, officiis
        culpa?
      </p>
      <Partnership
        v-for="(partner, i) in partners"
        :key="i"
        :partner="partner"
      />
    </div>
    <!-- FREE QUOTE -->
    <div class="free-quote-container">
      <div class="left-col">
        <h3>Building Inspiring Spaces</h3>
        <div class="secondline"></div>
        <p>
          quaerat suscipit, voluptatem beatae expedita numquam vitae corrupti
          labore aspernatur dolorem reprehenderit ullam?
        </p>
      </div>
      <div>
        <button><a href="#">GET A FREE QUOTE</a></button>
        <p class="buttontext">Only takes a few seconds!</p>
      </div>
    </div>
    <!-- CONTACT & INFO -->
    <div class="divider"></div>
    <div class="contacts-container">
      <!-- constructions -->
      <div class="construction">
        <img src="../assets/construction_logo.png" alt="" />
        <p>
          We are specialists in the constructions of unique and exclusive
          properties. Our work Inspires. We pride ourselves on delivering
          outstanding quality and design for leading clients across the world
        </p>
        <button><a href="#">LEARN MORE</a></button>
      </div>
      <!-- tweet -->
      <div>
        <h3>LATEST TWEETS</h3>
        <div class="tweetcard">
          <Twitter
            v-for="(tweet, tweetkey) in tweets"
            :key="tweetkey"
            :tweet="tweet"
          />
        </div>
      </div>
      <!-- contact -->
      <div>
        <h3>CONTACT US TODAY</h3>
        <ul>
          <li>
            <i class="fas fa-globe"></i>Corporate Location 1600 Amphiteathre
            Parkway London WC11BA
          </li>
          <li>
            <i class="fas fa-home"></i>
            Residential Location 9521 Broadsberry Avenue Paddington RC79ZA
          </li>
          <li><i class="fas fa-phone"></i>1.800.458.556 / 1.800.532.2112</li>
          <li><i class="far fa-envelope"></i>info@your-domain.com</li>
          <li>
            <i class="far fa-clock"></i>Monday - Friday: 9:00 AM - 6:00 PM
          </li>
          <li>
            <i class="far fa-clock"></i>Saturday - Sunday: 9:00 AM - 12:00 PM
          </li>
        </ul>
      </div>
      <!-- find us -->
      <div class="googlemap">
        <h3>FIND US</h3>
        <Map />
      </div>
    </div>
  </footer>
</template>

<script>
import Partnership from "./Partnership.vue";
import Twitter from "./Twitter.vue";
import Map from "./Map.vue";

export default {
  name: "Footer",
  components: {
    Partnership,
    Twitter,
    Map,
  },
  data() {
    return {
      partners: [
        {
          img: "home-logo11-219096700-320x202.png",
        },
        {
          img: "home-logo10-219096700-320x202.png",
        },
        {
          img: "home-logo2-219096700-320x202.png",
        },
        {
          img: "home-logo1-219096700-320x202.png",
        },
        {
          img: "home-logo9-219096700-320x202.png",
        },
      ],

      tweets: [
        {
          profilepic: "3a74ce3d0532b7773b174c45ca3bd05a_bigger.png",
          username: "ThemeFusion",
          logo: "image (1).svg",
          text: "Do you need sublime WordPress hosting for your next website? Take advantage of exclusive partner offers that we have secured just for you, & launch your site in seconds with #avanda on WP engine hosting & get 30% off this Black Friday bit.Ly/randomlink2020 ",
          img: "En2TRxLW4AEiWUN.jpeg",
          like: "image (2).svg",
          share: "image (3).svg",
          data: "22h ago",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
// PARTNERS
.partner-container {
  margin-top: 30px;

  h3 {
    margin: 30px;
    font-size: 30px;
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
// FREE QUOTE
.left-col {
  margin-left: 200px;
}
.free-quote-container {
  display: flex;
  justify-content: space-evenly;
  height: 350px;
  background-image: url("../assets/about-call-to-action-57862405.jpg");
  background-repeat: no-repeat;
  background-position: center center;

  text-align: start;

  h3 {
    color: white;
    font-size: 35px;
    margin-top: 100px;
    margin-right: 300px;
  }
  .secondline {
    border: 1px solid #fed03d;
    margin: 40px 0px;
    width: 40%;
    margin-left: 0;
  }
  p {
    color: white;
    font-size: 20px;
    width: 600px;
  }
  button {
    background-color: #fed03d;
    color: #534c35;
    border: none;
    width: 300px;
    height: 50px;
    margin: 150px 0 20px 40px;

    a {
      text-decoration: none;
      font-size: 20px;
    }
  }
  button:hover {
    background-color: #333333;
    cursor: pointer;
  }
  button:hover a {
    color: white;
  }
  .buttontext {
    margin-left: 40px;
  }
}

// CONTACT & INFO
.divider {
  background-color: #3f3f3f;
  height: 20px;
}

.contacts-container {
  display: flex;
  justify-content: space-between;
  height: 550px;
  background-color: #1e1e1e;
}

// constructions
.construction {
  text-align: start;
  width: 400px;
  color: #6f6f6f;

  img {
    margin: 30px;
  }
  p {
    margin: 30px;
  }
  button {
    margin: 30px;
    height: 50px;
    width: 200px;
    background-color: #fed03d;
    color: #534c35;

    a {
      text-decoration: none;
      font-size: 20px;
    }
  }
}

// tweet
.tweetcard {
  width: 400px;
  text-align: start;
}
// contacts
.contacts-container {
  h3 {
    color: #fed03d;
    font-size: 20px;
    margin: 30px;
    text-align: start;
  }
  ul {
    list-style: none;
    color: #6f6f6f;
    text-align: start;
    margin: 23px;

    li {
      margin: 13px;
      width: 400px;
      font-size: 15px;
    }

    i {
      margin: 10px;
    }
  }
}

// map
.googlemap {
  margin-right: 40px;
  width: 450px;
}
</style>