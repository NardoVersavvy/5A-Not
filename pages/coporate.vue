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
          <p>Coporate and Commercial</p>
        </div>
      </div>
    </header>
    <section class="practice-area-desc">
      <div class="container">
        <div class="wrapper" data-aos="slide-up">
          <div class="area-all">
            <div class="sample-title">
              <img src="../assets/Icons/coporate.svg" alt="" />
              <p>CORPORATE AND COMMERCIAL</p>
            </div>
            <div class="card">
              <p>
                5A Jurists Consultancy Group regularly works with domestic and
                international clients on business formation and financing as
                well as myriad corporate transactions, contracts, securities,
                mergers, acquisitions, and joint ventures. Our clients have come
                to rely on our practical problem-solving skills and our know-how
                to optimize opportunities when they arise. Our experience in
                drafting and reviewing contracts enables us to quickly and
                economically address complicated business issues. Since its
                beginning, 5A Jurists . 5A Jurists Consultancy Group regularly
                works with domestic and international clients on business
                formation and financing as well as myriad corporate
                transactions, contracts, securities, mergers, acquisitions, and
                joint ventures. Our clients have come to rely on our practical
                problem-solving skills and our know-how to optimize
                opportunities when they arise. Our experience in drafting and
                reviewing contracts enables us to quickly and economically
                address complicated business issues. Since its beginning, 5A
                Jurists .
              </p>
              <!-- <div class="button">
                <a href="" class="btn btn-rounded-darkerblue"
                  >View Practice Area</a
                >
              </div> -->
            </div>
          </div>
          <!-- <img class="practice-img"
            src="../assets/Image/practice2.jpg"
            alt=""
          /> -->
        </div>
      </div>
    </section>

    <section class="learn-more">
      <div class="container">
        <h2>LEARN MORE CORPORATE AND COMMERCIAL</h2>
        <div class="law">
          <div class="law-card" data-aos="zoom-out">
            <img class="area-img" src="../assets/Image/bussiess.jpg" alt="" />
            <div class="desc-area">
              <h4>Business Corporates</h4>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididun consectetur adipiscing elit, sed do
                eiusmod tempor incididun.Lorem ipsum dolor sit amet, consectetur
              </p>
              <div class="button">
                <a href="" class="btn btn-rounded-white">Read More</a>
              </div>
            </div>
          </div>
          <div class="law-card" data-aos="zoom-out">
            <img
              class="area-img"
              src="../assets/Image/intellectual.jpg"
              alt=""
            />
            <div class="desc-area">
              <h4>Protection of Intellectual Property</h4>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididun consectetur adipiscing elit, sed do
                eiusmod tempor incididun.Lorem ipsum dolor sit amet, consectetur
              </p>
              <div class="button">
                <a href="" class="btn btn-rounded-white">Read More</a>
              </div>
            </div>
          </div>
          <div class="law-card" data-aos="zoom-out">
            <img class="area-img" src="../assets/Image/contract.jpg" alt="" />
            <div class="desc-area">
              <h4>Consumer Complaints</h4>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
                eiusmod tempor incididun consectetur adipiscing elit, sed do
                eiusmod tempor incididun.Lorem ipsum dolor sit amet, consectetur
              </p>
              <div class="button">
                <a href="" class="btn btn-rounded-white">Read More</a>
              </div>
            </div>
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
  .space{
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
    background: url("../assets/Image/practicearea.jpg") rgba(3, 42, 86, 0.3)
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
  .practice-area-desc {
    margin-top: 8rem;

    .container {
      .wrapper {
        .area-all {
          .sample-title {
            display: flex;
            justify-content: left;
            align-items: center;
            gap: 1rem;
            img {
              width: 3rem;
            }
            p {
              @extend .text;

              font-size: 1rem;
              color: $A-darkerblue;
              font-weight: 600;
            }
          }
          .card {
            margin-top: 1.88rem;
            p {
              @extend .text;
              font-size: 1rem;
              color: $A-darkerblue;
              font-weight: 400;
            }
            .button {
              display: grid;
              place-content: left;
              margin-top: 1.88rem;
              a {
                @extend .text;
                color: #fff;
                font-size: 1rem;
              }
            }
          }
        }

        .practice-img {
          margin-top: 1.88rem;
        }
      }
    }
  }
  @include responsive($md) {
    .practice-area-desc {
      .container {
        .wrapper {
          .practice-img {
            margin-top: 0rem;
            width: 20rem;
            object-fit: cover;
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .practice-area-desc {
      margin-top: 10rem;
      .container {
        width: 100%-30%;
      }
    }
  }
  @include responsive($xl) {
    .practice-area-desc {
      margin-top: 10rem;
      .container {
        .wrapper {
          .area-all {
            .sample-title {
              img {
                width: 5rem;
              }
              p {
                font-size: 1.3rem;
              }
            }
            .card {
              p {
                margin-top: 3rem;
                font-size: 1.13rem;
              }
            }
          }
        }
      }
    }
  }
  .learn-more {
    margin-top: 8rem;
    .container {
      h2 {
        @extend .h2;
        color: $A-darkerblue;
        margin-bottom: 1.69rem;
        text-align: center;
      }
      .law {
        .law-card {
          margin-top: 2rem;
          .area-img {
            border-top-left-radius: 2rem;
            border-top-right-radius: 2rem;
          }
          .desc-area {
            padding: 1rem;
            background: #fff;
            border-bottom-left-radius: 2rem;
            border-bottom-right-radius: 2rem;

            box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.1);

            h4 {
              @extend .title;
              margin-top: 1rem;
              font-size: 1.3rem;
              color: $A-darkerblue;
              font-weight: 500;
              line-height: 1.5rem;
            }
            p {
              margin-top: 0.94rem;
              @extend .text;
              font-size: 1rem;
              color: $A-darkerblue;
              font-weight: 400;
            }
            .button {
              margin-top: 0.94rem;
              .btn {
                align-items: left;
              }
            }
          }
        }
      }
    }
  }
  @include responsive($md) {
    .learn-more {
      margin-top: 10rem;
      .container {
        h2 {
          margin-left: 10rem;
          margin-right: 10rem;
        }
        .law {
          display: grid;
          grid-template-columns: 1fr 1fr 1fr;
          gap: 1rem;
          .law-card {
            margin-top: 3rem;
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .learn-more {
      margin-top: 10rem;
      .container {
        h2 {
          margin-left: 15rem;
          margin-right: 15rem;
        }
        .law {
          .law-card {
            margin-top: 2rem;

            .desc-area {
              width: 88.6%;
            }
          }
        }
      }
    }
  }
  @include responsive($xxl) {
    .learn-more {
      .container {
        .law {
          display: grid;
          grid-template-columns: 1fr 1fr 1fr;
          gap: 1rem;
          .law-card {
            margin-top: 5rem;

            .desc-area {
              width: 85%;
            }
          }
        }
      }
    }
  }

}
</style>