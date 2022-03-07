<template>
    
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
              <p>Contact@5alawoffice.com | +25116504949</p>
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
              <li class="drop">
                <a href="practice" class="scroll-link drop-down-link"
                  >Sector & Practice Area</a
                >
                <ul class="sublinks">
                  <div class="corp-link">
                    <li>
                      <a href="coporate"> Coporate and Commercial</a>
                    </li>

                    <li><a href="power"> Power and Energy</a></li>
                    <li><a href="telecom">ICT & Telecom</a></li>

                    <li>
                      <a href="charity">Charities & Nonprofit </a>
                    </li>
                      <li>
                      <a href="mining">Mining</a>
                    </li>
                    <li>
                      <a href="employee">Employement and Immigration</a>
                    </li>
                     
                    <li><a href="tax"> Taxation</a></li>
                  </div>
                </ul>
              </li>

              <li>
                <a href="team" class="scroll-link">Teams</a>
              </li>
              <li class="drop">
                <a href="insight" class="scroll-link drop-down-link"
                  >Insight</a
                >
                <ul class="sublinks2">
                  <div class="corp-link">
                    <li>
                      <a href="publication"> Publication</a>
                    </li>
                    <li><a href="news">News</a></li>
                    <li><a href="blog">Blog</a></li>
                    <li><a href="journal">Journal</a></li>
                  </div>
                </ul>
              </li>
              <li>
                <a href="about" class="scroll-link">About Us</a>
              </li>
              <li><a href="contact" class="scroll-link">Contact Us</a></li>
              <li>
                <!-- <a href="publication"><img src="../assets/Icons/search1.svg" class="search" alt="" /></a>  -->
                <div class="input-container">
                  <button
                    @click="search"
                    type="submit"
                    name="submit"
                    class="search-button"
                  >
                    <img
                      src="../assets/Icons/search1.svg"
                      class="icon"
                      alt=""
                    />
                  </button>
                  <input
                    class="input-field"
                    type="search"
                    v-model="searchTerm"
                    placeholder="Search..."
                    name="search"
                  />
                </div>
              </li>
            </ul>
          </div>
        </div>
      </nav>
   
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
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
    async search() {
      try {
        await axios
          .post(
            "https://versavvymedia.com/5Aback/",
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
  created() {},
};
</script>

<style lang="scss">
.body-main{
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
              margin-bottom: 0.5rem;
              .input-container {
                display: flex;
                flex-direction: row-reverse;
                width: 13rem;
                height: 0.4rem;
                margin-bottom: 0rem;
                margin-right: -3rem;
                margin-left: -1rem;
                .search-button {
                  background: none;
                  border: none;
                  padding: 0;
                  margin: 0;
                }
                .icon {
                  height: 2.1rem;
                  padding: 5px;

                  min-width: 50px;
                  // background: #fff;
                  border: 2px solid $A-white;
                  border-start-end-radius: 20px;
                  border-end-end-radius: 20px;
                  border-left: none;
                }
                ::placeholder {
                  color: #fff;
                  opacity: 1; /* Firefox */
                }
                :-ms-input-placeholder {
                  /* Internet Explorer 10-11 */
                  color: #fff;
                }
                ::-ms-input-placeholder {
                  /* Microsoft Edge */
                  color: #fff;
                }
                .input-field {
                  width: 100%;
                  padding: 15px;
                  color: $A-white;
                  font-size: 1rem;
                  outline: none;
                  background: none;
                  border-style: solid;
                  border-color: $A-white;
                  border-start-start-radius: 20px;
                  border-end-start-radius: 20px;
                  border-right: none;
                }
              }
              .scroll-link {
                @extend .text-medium;
                font-size: 1rem;
                color: #fff;
              }
              .sublinks,
              .sublinks2 {
                margin: 1rem 0;

                color: $A-green;
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
 
  @include responsive($md) {
    header {
      .mid-moto {
        .container {
          .moto-wrapper {
            display: flex;
            justify-content: center;
            margin-top: 5rem;
            .rectangle {
              img {
                width: 18rem;
              }
            }
            .moto {
              margin-top: 10rem;
              p {
                font-size: 3rem;
                margin-top: 1rem;
                margin-left: -2rem;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
  
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
   
    
  }
  @include responsive($xl) {
   
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
              gap: 2rem;
              margin-top: 1rem;
              padding-left: 2rem;
              position: relative;
              li {
                .scroll-link {
                  color: #fff;
                }
                a {
                  font-size: .8rem;

                  &:hover {
                    color: $A-green;
                    font-size: 1rem;
                    font-weight: 600;
                  }
                }
              }

              .drop {
                .sublinks, .sublinks2 {
                  position: absolute;
                  width: auto;
               
                  background: $A-green;
                  padding: 1.2rem 1rem 1rem 0.5rem;
                  border-radius: 1rem;
                  display: none;
                  top: 60px;
                  h3 {
                    font-size: 1.13rem;
                    margin-bottom: 1.2rem;
                  }
                  li {
                    margin-bottom: 1rem;

                    width: 170px;
                    float: none;
                    display: list-item;
                    position: relative;
                    a {
                      color: $A-white;
                      font-size: 1rem;
                    }
                  }
                }
                  &:hover {
                       cursor: pointer;
      
        .sublinks{
                    display: block;
          margin-top: -1.8rem;
          
          width: 450px;
         left: 5.5rem;
          position: absolute;
        }
         .sublinks2{
                    display: block;
         margin-top: -1.8rem;
          
          width: 200px;
         left: 21rem;
          position: absolute;
        }
                  }
              }
            }
          }
        }
      }
      
    
  }
}


</style>