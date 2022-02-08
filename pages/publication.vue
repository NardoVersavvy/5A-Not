<template>
  <div class="body-main">
    <header id="app" class="header">
      <nav class="nav" id="nav">
        <div class="container banner">
          <div class="logo">
            <img src="../assets/Icons/Logo.svg" alt="" />
          </div>
          <div class="menu-bar menu">
            <hr />
            <hr />
            <hr />
          </div>

          <div class="links-container">
            <img src="../assets/Icons/close.svg" class="close-btn" alt="" />
            <div class="upper-nav">
              <p>Contact@5alawoffice.com | +25116504949|</p>
              <ul>
                <li>
                  <a href=""><img src="../assets/Icons/mail.svg" alt="" /> </a>
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/twitter.svg" alt="" />
                  </a>
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/facebook.svg" alt="" />
                  </a>
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/google.svg" alt="" />
                  </a>
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/linkedin.svg" alt="" />
                  </a>
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/youtube.svg" alt="" />
                  </a>
                </li>
              </ul>
              <div class="social"></div>
            </div>
            <ul class="nav-links">
              <li><a href="" class="scroll-link"> Home</a></li>

              <li class="drop-down">
                <a href="practice" class="scroll-link drop-down-link"
                  >Practice Area</a
                >

                <ul class="sublinks">
                  <div class="corp-link">
                    <li>
                      <a href="coporate"> Coporate and Commercial</a>
                    </li>
                    <li><a href="coporate">Banking & Finance</a></li>
                    <li><a href="coporate"> Power and Energy</a></li>
                    <li><a href="coporate">ICT & Telecom</a></li>

                    <li>
                      <a href="coporate">Charities & Nonprofit Organizations</a>
                    </li>
                    <li>
                      <a href="coporate">Employement and Immigration</a>
                    </li>
                    <li><a href="coporate"> Taxation</a></li>
                  </div>
                </ul>
              </li>

              <li>
                <a href="team" class="scroll-link">Teams</a>
              </li>
              <li class="drop-down2">
                <a href="publication" class="scroll-link drop-down-link2"
                  >Insights</a
                >
                <ul class="sublinks2">
                  <div class="corp-link2">
                    <li>
                      <a href=""> Journal</a>
                    </li>
                    <li><a href="">Publication</a></li>
                    <li><a href=""> Blog</a></li>
                    <li><a href="">News</a></li>
                  </div>
                </ul>
              </li>
              <li>
                <a href="about" class="scroll-link">About Us</a>
              </li>
              <li><a href="contact" class="scroll-link">Contact Us</a></li>
            </ul>
          </div>
        </div>
      </nav>
      <div class="mid-title">
        <div
          class="wrapper"
          data-aos="slide-left"
          data-aos-offset="20"
          data-aos-delay="50"
          data-aos-duration="1000"
          data-aos-mirror="true"
          data-aos-once="false"
          data-aos-anchor-placement="top-center"
        >
          <p>PUBLICATION</p>
        </div>
      </div>
    </header>
    <section class="links">
      <div class="container">
        <div class="link">
          <ul class="public-link">
            <li>
              <a href="#"> Laws</a>
            </li>
            <li><a href="#">Journal</a></li>
            <li><a href="#"> Article</a></li>
            <li><a href="#"> Research</a></li>
            <li><a href="#"> Proclamations</a></li>
          </ul>
        </div>
      </div>
    </section>
    <section class="publication-post">
      <div class="container">
        <div class="search">
          <div class="input-container">
            <button @click="search" type="submit" name="submit" class="search-button">
              <img src="../assets/Icons/search.svg" class="icon" alt="" />
            </button>
            <input
              class="input-field"
              type="search"
              v-model="searchTerm"
              placeholder="Search..."
              name="search"
            />
          </div>
          <div class="search-object">
            <ul class="search-list">
              <li>
                <a href=""> Coporate and Commercial</a>
              </li>
              <li><a href="">Power and Energy</a></li>
              <li><a href="">Banking & Finance</a></li>
              <li><a href="">ICT & Telecom</a></li>

              <li><a href="">M anufacturing and Industrial</a></li>
              <li><a href="">Charities & Nonprofit Organizations</a></li>
            </ul>
            <div class="recent-blog">
              <h2>Recent Publication</h2>
              <div class="wrapper">
                <div class="recent">
                  <img
                    class="blog-picture"
                    src="../assets/Image/blog.jpg"
                    alt=""
                  />
                  <p>Taxation</p>
                </div>
                <div class="recent">
                  <img
                    class="blog-picture"
                    src="../assets/Image/practice5.jpg"
                    alt=""
                  />
                  <p>Organizations Law</p>
                </div>
                <div class="recent">
                  <img
                    class="blog-picture"
                    src="../assets/Image/bussiess.jpg"
                    alt=""
                  />
                  <p>Mining</p>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div
          class="publcation-wrapper"
          v-for="row in allData"
          :key="row.post_id"
        >
          <div
            class="single-publication"
            data-aos="slide-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="img-wrapper">
              <div class="lists">
                <img class="pub-img" src="../assets/Image/pub.svg" alt="" />
                <div class="pub-title">{{ row.post_title }}</div>
              </div>
            </div>
            <div class="publication-desc">
              <h4>{{ row.post_title }}</h4>
              <p>
                {{ row.post_content }}
              </p>
            </div>
          </div>
          <div class="arrow">
            <img src="../assets/Icons/back.svg" alt="" />

            <img src="../assets/Icons/next.svg" alt="" />
          </div>
        </div>
      </div>
    </section>
    <section class="other-publication">
      <div class="container">
        <h2>Other Publications</h2>
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
          >
            <img class="pub-img" src="../assets/Image/pub2.svg" alt="" />
            <div class="pub-title">Womens Right in Ethiopia</div>
          </div>
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
          >
            <img class="pub-img" src="../assets/Image/pub3.svg" alt="" />
            <div class="pub-title">Crimal law in Ethiopia</div>
          </div>
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
          >
            <img class="pub-img" src="../assets/Image/pub4.svg" alt="" />
            <div class="pub-title">Contract of Mandate</div>
          </div>
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
          >
            <img class="pub-img" src="../assets/Image/pub2.svg" alt="" />
            <div class="pub-title">Childrens Law in Ethiopia</div>
          </div>
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
          >
            <img class="pub-img" src="../assets/Image/pub3.svg" alt="" />
            <div class="pub-title">Human Right</div>
          </div>
          <div
            class="lists"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <img class="pub-img" src="../assets/Image/pub4.svg" alt="" />
            <div class="pub-title">Democratic in Ethiopia</div>
          </div>
        </div>
      </div>
    </section>
    <section class="contact">
      <div class="container">
        <div class="contact-box">
          <div class="contact-hours">
            <h2>HOURS FOR CONTACT</h2>
            <p class="desc-p">
              This is the contact hours; please make sure your time is in sync
              with ours.
            </p>
            <div class="time-contact">
              <img src="../assets/Icons/time.svg" alt="" />
              <p>Monday-Thursday 6:00-19:00 GMT</p>
            </div>
            <div class="time-contact">
              <img src="../assets/Icons/time.svg" alt="" />
              <p>Firday-Staurday 7:00-18:00 GMT</p>
            </div>

            <div class="socials">
              <img src="../assets/Icons/decor.svg" alt="" />
              <ul>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/mail.svg" alt="" />
                    <p>Contact@5alawoffice.com</p></a
                  >
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/linkedin.svg" alt="" />
                    <p>5Alawoffice@linkedin.com</p></a
                  >
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/facebook.svg" alt="" />
                    <p>5Alawoffice@facebook.com</p></a
                  >
                </li>
                <li>
                  <a href=""
                    ><img src="../assets/Icons/phone.svg" alt="" />
                    <p>0116504949, Fax – 0116505758</p></a
                  >
                </li>
              </ul>
            </div>
          </div>

          <div class="contact-form">
            <h2>CONTACT US</h2>
            <p>
              This is the contact form; Please make sure to fill it in order for
              you to reach us
            </p>
            <form action="" class="myform">
              <img
                class="contact-decor"
                src="../assets/Icons/decor2.svg"
                alt=""
              />
              <div class="input-box">
                <input
                  type="text"
                  name="name"
                  class="line right-margin"
                  placeholder="Frist Name"
                />
                <input
                  type="email"
                  name="name"
                  class="line right-margin"
                  placeholder="Email"
                />

                <input
                  class="line right-margin"
                  type="text"
                  name="area"
                  placeholder="Select Area"
                />
                <input
                  type="text"
                  name="email"
                  class="line right-margin"
                  placeholder="Attachement"
                />
              </div>
              <textarea class="line" name="Message" id="" cols="30" rows="5">
Message
            </textarea
              >
              <!-- <div class="list-areas">
                <div>
                  <input type="checkbox" id="check1" name="practice1" checked />
                  <label for="scales">Practice1</label>
                </div>

                <div>
                  <input type="checkbox" id="check2" name="practice2" />
                  <label for="horns">Practice2</label>
                </div>
                <div>
                  <input type="checkbox" id="check2" name="practice3" />
                  <label for="horns">Practice3</label>
                </div>
              </div> -->
              <div class="submit-buttons">
                <a class="btn btn-white" href="#">SEND MESSAGE</a>
              </div>
            </form>
          </div>
        </div>
      </div>
    </section>

    <footer class="footer">
      <div class="container">
        <section class="footer-wrapper">
          <div class="footer-link-container">
            <div class="upper">
              <div class="map">
                <a href="">
                  <img src="../assets/Image/map.jpg" alt="" />
                </a>
              </div>
              <div class="desti">
                <h3 class="desti-title">Quick links</h3>
                <ul class="desti-list">
                  <div class="links">
                    <li class="footer-link"><a href="index">Home</a></li>
                    <li class="footer-link"><a href="about">About Us</a></li>
                    <li class="footer-link">
                      <a href="publication">Blog & News</a>
                    </li>
                    <li class="footer-link"><a href="#">Publication</a></li>
                    <li class="footer-link">
                      <a href="contact">Contact Us</a>
                    </li>
                    <li class="footer-link">
                      <a href="practice">Practice Areas</a>
                    </li>
                  </div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">About us</h3>
                <ul class="desti-list">
                  <div>
                    <p>
                      Ea eiusmod sit enim pariatur adipisicing nisi elit tempor
                      cupidatat deserunt et irure nulla. Aliqua labore cupidatat
                      nulla magna exercitation anim tempor consequat officia
                      mollit minim deserunt.
                    </p>
                  </div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">Contact Us</h3>
                <ul class="desti-list">
                  <div>
                    <p>
                      Ea eiusmod sit enim pariatur adipisicing nisi elit tempor
                      cupidatat deserunt et irure nulla. Aliqua labore cupidatat
                      nulla magna exercitation anim tempor consequat officia
                      mollit minim deserunt.
                    </p>
                    <div class="icon-container">
                      <img src="../assets/Icons/phone.svg" alt="" />
                      <img src="../assets/Icons/facebook.svg" alt="" />
                      <img src="../assets/Icons/linkedin.svg" alt="" />
                      <img src="../assets/Icons/mail.svg" alt="" />
                    </div>
                  </div>
                </ul>
              </div>
            </div>
          </div>
        </section>

        <hr />
        <div class="lower">
          <img src="../assets/Icons/Logo.svg" alt="" />
          <p>EXPERTISE. EXPERIENCE. EXCELLENCE.</p>
        </div>
        <div class="copyright">
          <p>
            All Rights Reserved.&copy; 2022 Web Design & Development by
            <a href="https://versavvymedia.com/">Versavvy Media PLC</a>
          </p>
        </div>
      </div>
    </footer>
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
      searchTerm: ''
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
    const dropDown = document.querySelector(".drop-down-link");
    const dropDownFull = document.querySelector(".nav-links");
    const sublinks = document.querySelector(".sublinks");
    console.log(sublinks);
    dropDown.addEventListener("mouseover", (e) => {
      const text = e.currentTarget.textContent;
      const tempBtn = e.currentTarget.getBoundingClientRect();
      const center = tempBtn.width / 2;
      sublinks.classList.add("show-links");
      // sublinks.style.left = `-${center + 5}px`
      console.log(center);
    });

    dropDownFull.addEventListener("mouseleave", () => {
      sublinks.classList.remove("show-links");
    });
    const dropDown2 = document.querySelector(".drop-down-link2");
    const dropDownFull2 = document.querySelector(".nav-links");
    const sublinks2 = document.querySelector(".sublinks2");
    console.log(sublinks2);
    dropDown2.addEventListener("mouseover", (e) => {
      const text = e.currentTarget.textContent;
      const tempBtn = e.currentTarget.getBoundingClientRect();
      const center = tempBtn.width / 2;
      sublinks2.classList.add("show-links2");
      // sublinks.style.left = `-${center + 5}px`
      console.log(center);
    });

    dropDownFull2.addEventListener("mouseleave", () => {
      sublinks2.classList.remove("show-links2");
    });

    const menu = document.querySelector(".menu");
    const sidebar = document.querySelector(".links-container");
    const close = document.querySelector(".close-btn");
    const banner = document.querySelector(".banner");
    menu.addEventListener("click", () => {
      sidebar.style.right = "0";
    });
    close.addEventListener("click", () => {
      sidebar.style.right = "-70vw";
    });
    const scrollLink = document.querySelectorAll(".scroll-link");
    window.addEventListener("load", () => {
      scrollLink.forEach((link) => {
        if (link.href === path) {
          link.style.color = "#71deb5";
          link.style.fontWeight = "bold";
        }
      });
    });

    window.addEventListener("scroll", () => {
      const nav = document.querySelector(".nav");
      const menu = document.querySelector(".menu");
      const logo = document.querySelector(".logo a");
      const navHeight = nav.getBoundingClientRect().height;
      const scrollHeight = window.pageYOffset;

      if (navHeight < scrollHeight) {
        nav.classList.add("fixed");
        logo.innerHTML = `<picture>
    <source media="(min-width:650px)" srcset=" ">
    <img src="../assets/Icons/Logo.svg " class=" " alt=" " />
  </picture>`;

        if (window.innerWidth > 768) {
          scrollLink.forEach((link) => {
            link.classList.add("black");
            if (link.href === path) {
              link.classList.remove("black");
              link.style.color = "#71deb5";
            }
          });
        }
      } else {
        nav.classList.remove("fixed");

        if (window.innerWidth > 768) {
          scrollLink.forEach((link) => {
            link.classList.remove("black");
          });
        }
      }
    });
  },
  methods: {
    async search(){
      try {
        await axios.post("https://versavvymedia.com/5Aback/", {
          action: "search",
          term: this.searchTerm
        }, config).then(res => {
          console.log(res.data);
          this.allData = res.data
        })
      } catch (err) {
        console.log(err.message);
      }
    },
    async fetchData() {
      

      try {
        await axios
          .post(
            "https://versavvymedia.com/5Aback/",
            {
              action: "fetchAll",
            },
            config
          )
          .then((res) => {
            console.log("response", res.data);
            this.allData = res.data;
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
          grid-template-columns: 1fr 1fr 1fr;
          gap: 2rem;
          li {
            a {
              @extend .text;
              font-size: 1rem;
              font-weight: 500;
              color: $A-darkerblue;
            }
          }
          &:hover {
            color: $A-lightblue;
            font-size: 1.3rem;
            font-weight: 600;
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
  @include responsive($lg) {
    .links {
      .container {
        .link {
          .public-link {
            display: flex;
            li {
              a {
                margin-left: 2rem;
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
          }
        }
      }
    }
  }
  .other-publication {
    margin-top: 8rem;
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
      margin-top: 10rem;
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
  .contact {
    margin-top: 8rem;
    .container {
      .contact-box {
        .contact-form {
          background: $A-darkerblue;
          padding: 1rem;
          padding-right: 3rem;
          margin-top: 5rem;
          position: relative;
          .contact-decor {
            position: absolute;
            right: 0.5rem;
            top: 0;
            width: 2rem;
            height: 70vh;
          }
          h2 {
            @extend .title;
            margin-top: 0.94rem;
            text-align: center;
            line-height: 1.3rem;
            color: #fff;
          }
          p {
            @extend .text;
            margin-top: 0.94rem;
            text-align: center;
            font-size: 0.8rem;
            line-height: 1.3rem;
            color: #e1e9f2;
          }
          .myform {
            place-content: center;

            input,
            textarea {
              background: $A-darkerblue;
              border: solid #fff;
              border-style: none;
              outline: none;
              width: 100%;
              margin-top: 1rem;
              border: none;
              border-bottom: 1px solid #fff;
            }
            input {
              color: #fff;

              &::placeholder {
                color: #fff;
              }
            }
            input[type="text"],
            input[type="email"] {
              padding: 1rem 0.8rem;
              color: #fff;
            }
            textarea {
              padding: 1rem 0.8rem;
              color: #ffff;
            }
            // .list-areas {
            //   div {
            //     input {

            //     }
            //   }
            // }

            .submit-buttons {
              margin-top: 5rem;
              display: flex;
              justify-content: center;
            }
          }
        }
        .contact-hours {
          background: url("../assets/Image/hours.jpg") rgba(42, 46, 83, 0.7)
            no-repeat;
          background-position: center;
          background-size: cover;
          background-blend-mode: overlay;
          // height: 70vh;
          margin-top: 5rem;
          padding: 1rem;
          h2 {
            @extend .title;
            margin-top: 0.94rem;
            text-align: left;
            color: #fff;
            line-height: 2rem;
          }
          .desc-p {
            @extend .text;
            margin-top: 0.94rem;
            text-align: left;
            font-size: 0.8rem;
            line-height: 1.3rem;
            color: #e1e9f2;
          }
          .time-contact {
            display: flex;
            align-items: center;
            margin-top: 0.8rem;
            p {
              @extend .text;

              text-align: left;
              margin-left: 1rem;
              color: #e1e9f2;
            }
          }
          .socials {
            display: flex;
            margin-top: 3rem;
            align-items: center;
            gap: 1rem;
            ul {
              li {
                a {
                  display: flex;
                  color: #e1e9f2;
                  margin-top: 2rem;
                  p {
                    margin-left: 0.94rem;
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .contact {
      .container {
        .contact-box {
          display: flex;
          .contact-form {
            background: $A-darkerblue;
            padding: 1rem;
            padding-right: 4rem;
            // height: 60vh;

            .contact-decor {
              width: 2.3rem;
            }
            h2 {
              margin-top: 0.94rem;
              text-align: center;
              color: #fff;
            }
            p {
              margin-top: 0.94rem;
              text-align: center;
              font-size: 0.8rem;
              line-height: 1.3rem;
              color: #e1e9f2;
            }
          }
          .contact-hours {
            // height: 65vh;
            margin-top: 5rem;
            padding: 1rem;
            // width: 100%;
            h2 {
              margin-top: 0.94rem;
              text-align: left;
              color: #fff;
            }
            .desc-p {
              margin-top: 0.94rem;
              text-align: left;
              font-size: 0.8rem;
              line-height: 1.3rem;
              color: #e1e9f2;
            }
            .time-contact {
              display: flex;
              align-items: center;
              margin-top: 0.8rem;
              p {
                text-align: left;
                margin-left: 1rem;
                color: #e1e9f2;
              }
            }
            .socials {
              display: flex;
              margin-top: 3rem;
              align-items: center;
              gap: 1rem;
              ul {
                li {
                  a {
                    display: flex;
                    color: #e1e9f2;
                    margin-top: 2rem;
                    p {
                      margin-left: 0.94rem;
                    }
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
    .contact {
      .container {
        .contact-box {
          display: flex;
          .contact-form {
            padding: 1rem;
            // height: 60vh;
            margin-top: 0rem;
            padding-right: 5rem;
            .contact-decor {
              margin-top: 1rem;
            }
            h2 {
              margin-top: 2.5rem;
              text-align: center;
              color: #fff;
            }
            p {
              margin-top: 0.94rem;
              text-align: center;
              font-size: 0.8rem;
              line-height: 1.3rem;
              color: #e1e9f2;
            }
          }
          .contact-hours {
            // height: 65vh;
            margin-top: 5rem;

            padding: 3rem;
            // width: 100%;
            h2 {
              margin-top: 0.94rem;
              text-align: left;
              color: #fff;
            }
            .desc-p {
              margin-top: 0.94rem;
              text-align: left;
              font-size: 0.8rem;
              line-height: 1.3rem;
              color: #e1e9f2;
            }
            .time-contact {
              display: flex;
              align-items: center;
              margin-top: 0.8rem;
              p {
                text-align: left;
                margin-left: 1rem;
                color: #e1e9f2;
              }
            }
            .socials {
              display: flex;
              margin-top: 3rem;
              align-items: center;
              gap: 1rem;
              ul {
                li {
                  a {
                    display: flex;
                    color: #e1e9f2;
                    margin-top: 2rem;
                    p {
                      margin-left: 0.94rem;
                    }
                  }
                }
              }
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .contact {
      margin-top: 10rem;
    }
  }
  .footer {
    background: $A-darkerblue;
    margin-top: 6.25rem;

    .container {
      // width: 100%;
      .footer-wrapper {
        .footer-link-container {
          .upper {
            display: grid;
            // grid-template-columns: 1fr 1fr;
            place-items: center;
            .map {
              display: flex;
              justify-content: center;
              img {
                margin-top: 1rem;
              }
            }
            .desti {
              .desti-title {
                color: #fff;
                @extend .title;
                margin-top: 4.37rem;
                text-align: center;
                font-size: 1.13rem;
                font-weight: 500;
                text-transform: uppercase;
              }
              .desti-list {
                text-align: center;
                margin-top: 1.88rem;
                margin-bottom: 1.88rem;
                // margin-left: 2rem;
                // gap: 3.31rem;
                .links {
                  display: grid;

                  grid-template-columns: 1fr 1fr;
                  place-items: left;
                  gap: 1.88rem;

                  li {
                    a {
                      font-size: 0.8rem;
                    }
                  }
                }
                div {
                  // display: grid;
                  // place-items: left;
                  gap: 1rem;
                  margin-top: 0.8rem;

                  .footer-link {
                    a {
                      color: #fff;
                      font-size: 0.8rem;
                    }
                  }
                  p {
                    color: #fff;
                    @extend .text;

                    text-align: center;
                    font-size: 0.8rem;
                  }
                  .icon-container {
                    display: flex;
                    // align-items: center;
                    justify-content: center;
                    gap: 1.88rem;
                    margin-top: 0.88rem;
                  }
                }
              }
            }
          }
        }
      }
      hr {
        margin-top: 4.37rem;
        color: #fff;
      }
      .lower {
        display: grid;
        place-items: center;
        margin-top: 4.37rem;
        // margin-bottom: 5rem;
        img {
          width: 12rem;
        }
        p {
          color: #fff;
          font-size: 1rem;
          margin-top: 1.88rem;
          line-height: 1.3rem;
          text-align: center;
        }
      }
      .copyright {
        display: grid;
        place-items: center;
        margin-top: 5.37rem;

        p {
          color: #fff;
          font-size: 0.88rem;
          margin-top: 1.88rem;
          line-height: 1.3rem;
          text-align: center;
          a {
            color: $A-lightblue;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .footer {
      .container {
        .footer-wrapper {
          .footer-link-container {
            display: flex;
            // align-items: center;

            .upper {
              display: grid;
              grid-template-columns: 1fr 1fr;
              place-items: center;
              .map {
                margin-top: 4.37rem;
                img {
                  width: 50rem;
                }
              }
              .desti {
                .desti-title {
                  text-align: center;
                }
                .desti-list {
                  text-align: left;
                  margin-top: 0.98rem;
                  margin-bottom: 0.98rem;

                  div {
                    display: grid;
                    grid-template-columns: 1fr;
                    gap: 1.3rem;
                    margin-top: 0.98rem;
                    .footer-link {
                      a {
                        font-size: 1rem;
                        text-align: left;
                      }
                    }
                  }
                }
              }
            }
          }
        }

        .lower {
          img {
            width: 15rem;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .footer {
      margin-top: 8.13rem;
      .container {
        .footer-wrapper {
          .footer-link-container {
            place-items: center;
            .upper {
              gap: 4rem;
              .desti {
                .desti-title {
                  text-align: center;
                }
                .desti-list {
                  text-align: center;
                  margin-top: 0.98rem;
                  margin-bottom: 0.98rem;
                }
              }
            }
          }
        }

        .lower {
          margin-bottom: 0rem;
          display: flex;
          justify-content: space-between;
          img {
            margin-bottom: 1rem;
            // width: 20rem;
          }
          p {
            font-size: 1.3rem;
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .footer {
      margin-top: 10rem;
      .container {
        .footer-wrapper {
          display: flex;
          justify-content: center;
          align-items: flex-start;
          gap: 5rem;
          .footer-link-container {
            .upper {
              display: grid;
              grid-template-columns: 1fr 1fr 1fr 1fr;
              align-items: flex-start;
              gap: 5rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .footer {
      .container {
        .footer-wrapper {
          gap: 10rem;
          .footer-link-container {
            .upper {
              gap: 10rem;
            }
          }
        }
      }
    }
  }
}
</style>
