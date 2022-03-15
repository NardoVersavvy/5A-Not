<template>
  <div class="body-main">
    <header id="app" class="header">
      <NavApp />
      <div class="mid-title">
        <div
          class="wrapper"
          data-aos="slide-right"
          data-aos-offset="20"
          data-aos-delay="50"
          data-aos-duration="1000"
          data-aos-mirror="true"
          data-aos-once="false"
          data-aos-anchor-placement="top-center"
        >
          <p>Insights</p>
        </div>
      </div>
    </header>
    <section class="links">
      <div class="container">
        <div class="link">
          <ul class="public-link">
            <li>
              <a href="journal"
                >Journal
                <hr/> </a>
            </li>
            <li><a href="blog"> Blog   <hr/></a></li>
            <li><a href="news"> News   <hr/></a></li>
            <li><a href="publication"> Publication   <hr/></a></li>
          </ul>
        </div>
      </div>
    </section>

    <section class="other-publication">
      <div class="container">
        <h2></h2>
        <div class="wrapper">
          <div
            data-tilt
            class="lists"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
            v-for="post in allData" :key="post.id"
          >
            <img class="pub-img" :src="'http://localhost:8080/5A/post_img' + post.post_image" alt="" />
            <div class="pub-title">{{ post.post_title }}</div>
          </div>
         
        </div>
      </div>
    </section>
    <section class="space"></section>
    <ContactApp />
    <section class="space"></section>
    <FooterApp />
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
import axios from "axios";

const config = {
  headers: {
    Accept: "application/json",
    "Access-Control-Allow-Origin": "*",
    "Access-Control-Allow-Methods": "GET,POST,OPTIONS,DELETE,PUT",
  },
};
export default {
  data() {
    return {
      allData: [],
      searchTerm: "",
    };
  },
  mounted() {
    AOS.init({
      duration: 900,
      offset: 120,
      easing: "ease",
      once: false,
      anchorPlacement: "top-bottom",
    });
    var Tawk_API = Tawk_API || {},
      Tawk_LoadStart = new Date();
    (function () {
      var s1 = document.createElement("script"),
        s0 = document.getElementsByTagName("script")[0];
      s1.async = true;
      s1.src = "https://embed.tawk.to/62220908a34c245641296e76/1ftaf6j28";
      s1.charset = "UTF-8";
      s1.setAttribute("crossorigin", "*");
      s0.parentNode.insertBefore(s1, s0);
    })();

   
  },
  methods: {
    async search() {
      try {
        await axios
          .post(
            "https://5alawoffice.com/5Aback/",
            {
              action: "search",
              term: this.searchTerm,
            },
            config
          )
          .then((res) => {
            console.log(res.data);
            this.allData = res.data;
          });
      } catch (err) {
        console.log(err.message);
      }
    },
    async fetchData() {
      try {
        await axios
          .post(
            "/api/",
            {
              action: "fetchAll",
            },
            config
          )
          .then((res) => {
            console.log("response", res.data);
            this.allData = res.data;
            console.log(this.allData);
          });
      } catch (err) {
        console.log(err);
      }
    },
  },
  created() {
    this.fetchData();
  },
};
</script>

<style lang="scss" scoped>
.body-main {
  .space {
    margin-top: 8rem;
  }
  .show-links,
  .show-links2 {
    display: flex !important;
  }
  .fixed {
    position: fixed !important;
    top: 0;
    width: 100%;
    padding-bottom: 0.5rem;
    background: $A-darkerblue;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
    z-index: 999999;
  }
  header {
    background: url("../assets/Image/publication.jpg") rgba(3, 42, 86, 0.3)
      no-repeat;
    background-position: center center;
    background-size: cover;
    background-blend-mode: overlay;
    height: 70vh;
    width: 100%;

    nav {
      .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        .logo {
          margin-top: 1rem;
          img {
            width: 11rem;
          }
        }
        .menu-bar {
          margin-top: 1rem;
          hr {
            margin: auto;
            margin-top: 0.5rem;
            color: $A-white;
            border-style: solid;
            width: 2.35rem;
          }
        }
        .links-container {
          position: fixed;
          top: 0;
          right: -70vw;
          height: 100vh;
          width: 70vw;
          background: $A-darkerblue;
          z-index: 9999999999;
          transition: $trans;
          .upper-nav {
            display: none;
          }
          .close-btn {
            padding: 1rem;
            width: 5rem;
            position: absolute;
            top: 0rem;
            right: 0rem;
          }
          .nav-links {
            height: 50%;
            padding-top: 25rem;
            display: flex;
            flex-direction: column;
            justify-content: space-around;
            padding-left: 2rem;
            .drop-down2 {
              a {
                color: #fff;
              }
            }
            li {
              margin-bottom: 1rem;
              .scroll-link {
                @extend .text-medium;
                font-size: 1rem;
                color: #fff;
              }
              .sublinks,
              .sublinks2 {
                margin: 1rem 0;

                color: $A-white;
                h3 {
                  font-family: "medium bt";
                  font-weight: 500;
                  font-size: 1rem;
                  line-height: 1.5rem;
                  margin-bottom: 1rem;
                }
                img {
                  width: 1.2rem;
                }
                li {
                  margin-bottom: 0.5rem;
                  margin-left: 1rem;
                  a {
                    font-family: "light bt";
                    font-size: 0.88rem;
                    display: flex;
                    gap: 0.5rem;
                    color: $A-white;
                    transition: color 0.2s linear;
                    img {
                      width: 0.5rem;
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
    .mid-title {
      display: grid;
      place-content: center;
      .wrapper {
        margin-top: 15rem;
        p {
          margin-top: 0.94rem;
          font-size: 2rem;
          color: $A-white;
          font-weight: 700;
          text-transform: uppercase;
        }
      }
    }
  }
  @include responsive($md) {
    header {
      nav {
        .container {
          .links-container {
            width: 30vh;
            .close-btn {
              width: 6rem;
            }
            .nav-links {
              padding-top: 15rem;
            }
          }
        }
      }
      .mid-title {
        .wrapper {
          margin-top: 15rem;
          p {
            font-size: 2.3rem;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    header {
      nav {
        .container {
          .links-container {
            width: 30vh;
            .close-btn {
              width: 6rem;
            }
            .nav-links {
              padding-top: 15rem;
            }
          }
        }
      }
      .mid-title {
        .wrapper {
          margin-top: 20rem;
        }
      }
    }
  }
  @include responsive($xl) {
    header {
      nav {
        .container {
          .logo {
            img {
              width: 15rem;
            }
          }
          .menu-bar {
            display: none;
          }
          .links-container {
            display: block;
            position: static;
            // width: 50%;
            height: auto;
            z-index: 9999999999;
            transition: $trans;
            background: none;
            width: auto;
            .close-btn {
              display: none;
            }
            .upper-nav {
              display: flex;
              justify-content: space-between;
              margin-top: 1.5rem;
              padding-left: 2rem;
              gap: 3rem;
              p {
                color: #fff;
                font-size: 1rem;
              }
              ul {
                display: flex;
                gap: 1rem;
              }
            }
            .nav-links {
              height: auto;
              display: flex;
              padding-top: 0%;
              flex-direction: row;
              gap: 3rem;
              margin-top: 1rem;
              padding-left: 2rem;
              position: relative;
              li {
                .scroll-link {
                  color: #fff;
                }
                a {
                  font-size: 1rem;

                  &:hover {
                    color: $A-lightblue;
                    font-size: 1.13rem;
                    font-weight: 600;
                  }
                }
              }
              .drop-down {
                .sublinks {
                  position: absolute;
                  width: auto;
                  display: flex;
                  background: $A-darkerblue;
                  padding: 1.2rem 1rem 1rem 0.5rem;
                  border-radius: 1rem;
                  display: none;
                  h3 {
                    font-size: 1.13rem;
                    margin-bottom: 1.2rem;
                  }
                  li {
                    margin-bottom: 1rem;
                    a {
                      color: $A-white;
                      font-size: 1rem;
                    }
                  }
                }
              }
              .drop-down2 {
                .sublinks2 {
                  position: absolute;
                  width: auto;
                  display: flex;
                  background: $A-darkerblue;
                  padding: 1.2rem 1rem 1rem 0.5rem;
                  border-radius: 1rem;
                  display: none;
                  h3 {
                    font-size: 1.13rem;
                    margin-bottom: 1.2rem;
                  }
                  li {
                    margin-bottom: 1rem;

                    a {
                      color: $A-white;
                      font-size: 0.9rem;
                    }
                  }
                }
              }
            }
          }
        }
      }
      .mid-title {
        .wrapper {
          margin-top: 15rem;
          p {
            font-size: 3rem;
          }
        }
      }
    }
  }
  .links {
    margin-top: 3rem;
    .container {
      display: grid;
      place-items: center;

      .link {
        .public-link {
          display: grid;
          grid-template-columns: 1fr 1fr;
          place-items: center;
          gap: 1rem;
          li {
            display: grid;

            place-items: center;

            padding: 5px;
            width: 10rem;
            border-radius: 0px;
            a {
              @extend .text;

              font-size: 1.4rem;
              font-weight: 600;
              color: $A-darkerblue;
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .links {
      .container {
        .link {
          .public-link {
            display: flex;
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .links {
      .container {
        .link {
          .public-link {
            display: flex;
            gap: 2rem;
            li {
              width: 12rem;

              a {
                font-size: 1.1rem;
                margin-left: 0rem;
                hr {
                  display: none;
                }
                &:hover {
                  color: $A-green;
                  hr {
                    margin-top: 1rem;
                    display: block;
                    width:80%;
                    border-style: solid;
                    color: $A-green;
                  top: 0;
    right: 0vw;
    transition: all 0.3s linear;
    
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  .publication-post {
    margin-top: 5rem;
    .container {
      .publcation-wrapper {
        background: #ecf2fd;
        padding: 1rem;
        position: relative;
        .single-publication {
          .img-wrapper {
            .lists {
              display: grid;
              place-items: center;
              position: relative;
              margin-top: 2rem;

              .pub-img {
                // position: relative;
              }
              .pub-title {
                position: absolute;
                // top: 0;
                margin-left: 2rem;
                margin-right: 2rem;
                @extend .title;

                text-align: center;
                color: #fff;
              }
            }
          }
          .publication-desc {
            margin-top: 2rem;
            h4 {
              @extend .title;
              font-weight: 500;
              color: $A-darkerblue;
              text-align: center;
              line-height: 2rem;
            }
            p {
              @extend .text;
              margin-top: 0.94rem;
              color: $A-darkerblue;
            }
          }
        }
        .arrow {
          display: flex;
          justify-content: right;
          margin-top: 5rem;
          img {
            width: 3rem;
          }
        }
      }
      .search {
        // display: grid;
        // place-items: center;

        margin-top: 5rem;
        .input-container {
          display: flex;

          flex-direction: row-reverse;
          width: 15.38rem;
          margin-bottom: 2.13rem;

          .search-button {
            background: none;
            border: none;
            padding: 0;
            margin: 0;
          }
          .icon {
            padding: 10px;
            min-width: 50px;
            // background: #fff;
            border: 2px solid $A-darkerblue;
            border-left: none;
          }
          .input-field {
            width: 100%;
            padding: 10px;
            outline: none;
            background: none;
            border-color: #10284a;
            border-right: none;
          }
        }
        .search-object {
          margin-top: 0rem;
          margin-bottom: 5rem;
          .search-list {
            li {
              margin-top: 0.94rem;
              // text-transform: lowercase;
              a {
                color: $A-darkerblue;
              }
            }
          }
          .recent-blog {
            margin-top: 5rem;
            h2 {
              @extend .title;
              margin-top: 0.94rem;
              font-size: 1.5rem;
              text-align: center;
              color: $A-darkerblue;
            }
            .wrapper {
              .recent {
                display: flex;
                align-items: center;
                gap: 2rem;
                margin-top: 2rem;
                .blog-picture {
                  width: 5rem;
                  height: 5rem;
                  object-fit: cover;
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .publication-post {
      .container {
        display: flex;
        flex-direction: row-reverse;
        gap: 1rem;
        .publcation-wrapper {
          padding: 1rem;
          .single-publication {
            .publication-desc {
              margin-top: 4rem;
              p {
                margin-top: 2rem;
              }
            }
          }
        }
        .search {
          margin-top: 0rem;
          position: sticky;
          top: 0;
          .search-object {
            .recent-blog {
              .wrapper {
                .recent {
                  display: flex;
                  align-items: center;
                  gap: 2rem;
                  margin-top: 2rem;
                  .blog-picture {
                    width: 5rem;
                    height: 5rem;
                    object-fit: cover;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .publication-post {
      margin-top: 10rem;
      .container {
        gap: 3rem;
        .publcation-wrapper {
          padding-left: 5rem;
          padding-right: 5rem;
          .single-publication {
            .publication-desc {
              margin-top: 4rem;
              p {
                margin-top: 2rem;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .publication-post {
      margin-top: 10rem;
      .container {
        .publcation-wrapper {
          padding-left: 5rem;
          padding-right: 5rem;
          padding-top: 5rem;
          padding-bottom: 5rem;
          .single-publication {
            .publication-desc {
              margin-top: 4rem;
              p {
                margin-top: 2rem;
              }
            }
          }
        }
        .search {
          .search-object {
            margin-top: 1rem;
          }
        }
      }
    }
  }
  .other-publication {
    margin-top: 5rem;
    .container {
      h2 {
        @extend .title;
        margin-top: 0.94rem;
        text-align: center;
        color: $A-darkerblue;
      }
      .wrapper {
        .lists {
          display: grid;
          place-items: center;
          position: relative;
          margin-top: 2rem;

          .pub-img {
            padding: 0;
            // position: relative;
          }
          .pub-title {
            position: absolute;
            // top: 0;
            margin-left: 2rem;
            margin-right: 2rem;
            @extend .text;
            font-size: 1.5rem;
            margin-top: 0.94rem;
            text-align: center;
            color: #fff;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .other-publication {
      .container {
        .wrapper {
          display: flex;
          gap: 1rem;
          margin-top: 3rem;
          .lists {
            .pub-title {
              font-size: 1.3rem;
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .other-publication {
      .container {
        .wrapper {
          display: grid;
          grid-template-columns: 1fr 1fr 1fr;
          gap: 1rem;
          margin-top: 3rem;
          .lists {
            .pub-title {
              font-size: 1.3rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .other-publication {
      .container {
        .wrapper {
          margin-top: 5rem;
          .lists {
            .pub-title {
              margin-left: 5rem;
              margin-right: 5rem;
              font-size: 1.7rem;
            }
          }
        }
      }
    }
  }
}
</style>
