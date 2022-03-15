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
          <p>CONTACT US</p>
        </div>
      </div>
    </header>

   <ContactApp />
    <!-- <section class="map">
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3940.7913028528865!2d38.78135341478628!3d8.991342293546982!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x164b85f52615ebdf%3A0x6a0949274cd951c7!2sTropical%20Mall!5e0!3m2!1sen!2sus!4v1643637951202!5m2!1sen!2sus"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
      ></iframe>
    </section> -->
    <section class="map">
      <h1 class="map-title text-center">Map</h1>
      <div class="map-container">
        <div class="location">
          <div class="map-responsive">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3940.7913028528865!2d38.78135341478628!3d8.991342293546982!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x164b85f52615ebdf%3A0x6a0949274cd951c7!2sTropical%20Mall!5e0!3m2!1sen!2sus!4v1643637951202!5m2!1sen!2sus"
              style="border: 0"
              allowfullscreen=""
              loading="lazy"
            ></iframe>
          </div>
        </div>
      </div>
    </section>
    <FooterApp />
  </div>
</template>

<script>
import AOS from "aos";
import "aos/dist/aos.css";
export default {
  mounted() {
    AOS.init({
      duration: 900,
      offset: 120,
      easing: "ease",
      once: false,
      anchorPlacement: "top-bottom",
    });
       var Tawk_API=Tawk_API||{}, Tawk_LoadStart=new Date();
(function(){
var s1=document.createElement("script"),s0=document.getElementsByTagName("script")[0];
s1.async=true;
s1.src='https://embed.tawk.to/62220908a34c245641296e76/1ftaf6j28';
s1.charset='UTF-8';
s1.setAttribute('crossorigin','*');
s0.parentNode.insertBefore(s1,s0);
})();

 
  },
  created() {},
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
    background: url("../assets/Image/contact.jpg") rgba(3, 42, 86, 0.3)
      no-repeat;
    background-position: center center;
    background-size: cover;
    background-blend-mode: overlay;
    height: 70vh;
    width: 100%;

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
     
      .mid-title {
        .wrapper {
          margin-top: 20rem;
        }
      }
    }
  }
  @include responsive($xl) {
    header {
    
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
  .map {
    margin-top: 8rem;
    overflow: hidden;
    padding-bottom: 5.06rem;
    height: 31.94rem;

    .map-title {
      @extend .h2;
      margin-bottom: 4.88rem;
      color: $A-darkerblue;
    }
    .map-container {
      .location {
        .map-responsive {
          overflow: hidden;
          padding-bottom: 56.25%;
          position: relative;
          height: 17rem;

          max-height: 31.94rem;
          iframe {
            left: 0;
            top: 0;
            height: 100%;
            width: 100%;
            position: absolute;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    height: 51.94rem;
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
                  margin-top: 0.98rem;
                  margin-bottom: 0.98rem;

                  div {
                    display: grid;
                    grid-template-columns: 1fr;
                    gap: 1.3rem;
                    margin-top: 0.98rem;
                    .footer-link {
                      a {
                        font-size: 0.8rem;
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