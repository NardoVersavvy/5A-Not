<template>
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
                    <li class="footer-link"><a href="#">Home</a></li>
                    <li class="footer-link"><a href="about">About Us</a></li>
                    <li class="footer-link"><a href="practice">Practice </a></li>
                    <li class="footer-link"><a href="publication">Publication</a></li>
                    <li class="footer-link"><a href="publication">News</a></li>
                    <li class="footer-link"><a href="contact">Contact Us</a></li>
                  </div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">About us</h3>
                <ul class="desti-list">
                  <div>
                    <p>
                    5A is an Ethiopian consulting firm that aspires to be a full-service firm. With a legal team that has over 30 years of experience in advising and representing clients on a wide range of legal matters relating to business and investment in the country.
                    </p>
                  </div>
                </ul>
              </div>

              <div class="desti">
                <h3 class="desti-title">Contact Us</h3>
                <ul class="desti-list">
                  <div>
                    <p>
                     Tropical mall 9th floor @

Bole Road

Around Ramada Hotel
<br/>
Addis Ababa, Ethiopia<br/>
                    </p>
                    <div class="icon-container">
                     <a href="#"><img src="../assets/Icons/phone.svg" alt="" /></a> 
                      <a href="#"><img src="../assets/Icons/facebook.svg" alt="" /></a>
                     <a href="#"><img src="../assets/Icons/linkedin.svg" alt="" /></a> 
              <a href="#"><img src="../assets/Icons/mail.svg" alt="" /></a>
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
</template>

<script>
export default {

}
</script>

<style lang="scss">
.space{
  margin-top: 8rem;

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
        margin-top: 1.37rem;
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
                  margin-top: 1rem;
                  margin-bottom: 0.98rem;

                  div {
                    display: grid;
                    grid-template-columns: 1fr;
                    gap: 1.3rem;
                    margin-top: 1rem;
                    .footer-link {
                      a {
                       
                        font-size: .8rem;
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
              gap: 2rem;
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
              gap: 5rem;
            }
          }
        }
      }
    }
  }
</style>