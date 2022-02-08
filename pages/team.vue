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
          <p>MEET OUR TEAM</p>
        </div>
      </div>
    </header>
    <section class="stand">
      <div class="container">
        <div
          class="stand-content"
          data-aos="fade-up"
          data-aos-offset="20"
          data-aos-delay="50"
          data-aos-duration="1000"
          data-aos-mirror="true"
          data-aos-once="false"
          data-aos-anchor-placement="top-center"
        >
          <h1>WHAT OUR TEAM STANDS FOR</h1>
          <p>
            Conceived and formally established by Ali, Almaw, Alemu, Amare &
            Ashenafi (5A Jurists Consultancy Group PLC) is an aspiring
            full-service consultancy office in Ethiopia. With prominent lawyers
            and legal team that has over and above 30 years of experience in
            consulting and representing clients on a wide range of legal issues
            concerning business and investment in the country, our consultancy
            firm has begun to make its early influence felt on the Ethiopian
            legal system. We are committed to treating each of our clients with
            courtesy, respect and compassion – regardless of the size of their
            case. We are a firm that will be here in the future, which we’ve
            guaranteed with a succession plan to maintain our exemplary service
            to you for decades to come.
          </p>
          <div class="button">
            <a href="" class="btn btn-rounded-darkerblue">Contact Today!</a>
          </div>
        </div>
      </div>
    </section>
    <!-- <section class="picture">
      <div class="wrapper" data-aos="fade-up">
        <img class="team-img" src="../assets/Image/team2.JPG" alt="" />
        <img class="team-decor" src="../assets/Icons/teamdecor.svg" alt="" />
      </div>
    </section> -->

    <div class="pop-up" v-if="showPopup" @click.self="togglePopup">
      <div class="inner">
        <img
          src="../assets/Icons/close.svg"
          class="close-modal-btn"
          @click.self="togglePopup"
          alt=""
        />
        <div class="bio">
          <img class="decor" src="../assets/Icons/decor3.svg" alt="" />
          <img class="indiv-img" :src="modalData.img" alt="" />

          <h4>{{ modalData.name }}</h4>
          <p>
            {{ modalData.desc }}
            <br />
            <br />
            <a href=""> Contact information – {{ modalData.contact }}</a>
          </p>
        </div>
      </div>
    </div>
    <section class="topdecor">
      <div class="left">
        <img class="left-decor" src="../assets/Icons/leftdecor.svg" alt="" />
        <img class="edge-decor1" src="../assets/Icons/edge1.svg" alt="" />
        <h2>Meet the Team</h2>
      </div>

      <img class="pass-decor" src="../assets/Icons/meetdecor.svg" alt="" />
      <div class="right">
        <img class="decor" src="../assets/Image/team2.JPG" alt="" />
        <img class="edge-decor" src="../assets/Icons/edge4.svg" alt="" />
      </div>
    </section>
    <section class="meet-team">
      <div class="container">
        <!-- <h2>Meet the Team</h2> -->
        <div class="team-wrapper">
          <div
            @click="togglePopup('ali')"
            class="card"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/Ali.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Ali Mohammed Ali</h4>
              <p>
                Ali Mohammed Ali has earned his Bachelor of Law /LL. B/ from
                Addis Ababa University, and his Master of Laws /LL.M/ from...
              </p>
            </div>
          </div>
          <div
            @click="togglePopup('amare')"
            class="card"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/Amare.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Amare Ashenafi</h4>
              <p>
                Amare earned his law degree (LLB) from Bahir Dar University, his
                LLM from Mekelle University in Tax and ...
              </p>
            </div>
          </div>
          <div
            @click="togglePopup('alemu')"
            class="card"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/Alemu.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Alemu Korme</h4>
              <p>
                Alemu earned his law degree (LLB) from Addis Ababa University,
                his MBA from Lead Star University in...
              </p>
            </div>
          </div>
          <div
            @click="togglePopup('almaw')"
            class="card"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/Almaw.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Almaw Wolie</h4>
              <p>
                Almaw has received his Bachelor of Laws /LL. B/ from Addis Ababa
                University in July 2000 and his Master...
              </p>
            </div>
          </div>
          <div
            class="card"
            @click="togglePopup('ashenafi')"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img
                class="indiv-img"
                src="../assets/Image/Ashenafi.jpg"
                alt=""
              />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Ashenafi Yirga</h4>
              <p>
                A graduate of the Law School of Bahir Dar University as an
                outstanding student, Ashenafi heads the...
              </p>
            </div>
          </div>

          <div
            class="card"
            @click="togglePopup('mesnbet')"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/mesnbet.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Dr. Mesnbet Assefa</h4>
              <p>
                Mesenbet earned his LL.B from Bahir Dar University in 2006 and
                graduated with distinction. He further...
              </p>
            </div>
          </div>

          <div
            class="card"
            @click="togglePopup('hanna')"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/hanna.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Hanna Yohannas</h4>
              <p>
                Hanna Yohannes is an assistant lawyer and office manager at 5A
                Jurists Consultancy Group. First, Appointed...
              </p>
            </div>
          </div>
          <div
            class="card"
            @click="togglePopup('linora')"
            data-aos="zoom-out-up"
            data-aos-offset="20"
            data-aos-delay="50"
            data-aos-duration="1000"
            data-aos-mirror="true"
            data-aos-once="false"
            data-aos-anchor-placement="top-center"
          >
            <div class="indiv-pic">
              <img class="indiv-img" src="../assets/Image/linora.jpg" alt="" />
              <div class="bottom-decor"></div>
            </div>
            <div class="name">
              <h4>Linora Mohammed</h4>
              <p>
                Assistant Lawyer of 5A, Linora earned her law degree (LLB) from
                Adigrat University as an outstanding student.
              </p>
            </div>
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
                    <li class="footer-link"><a href="#">Home</a></li>
                    <li class="footer-link"><a href="about">About Us</a></li>
                    <li class="footer-link"><a href="#">Practice Areas</a></li>
                    <li class="footer-link"><a href="#">Publication</a></li>
                    <li class="footer-link"><a href="#">News</a></li>
                    <li class="footer-link"><a href="#">Contact Us</a></li>
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
export default {
  data() {
    return {
      modalData: {},
      ali: {
        id: 1,
        img: require("../assets/Image/Ali.jpg"),
        name: "Ali Mohammed Ali",
        desc: "Founder and Managing Partner of 5A, Ali Mohammed Ali has earned his Bachelor of Law /LL. B/ from Addis Ababa University, and his Master of Laws /LL.M/ from Stockholm University.First, he was appointed as a High Court Judge and served for 5 years, and then he was upgraded to the Amhara National Regional State Supreme Court where he served for about 10 years.He was then appointed as Head of Amhara National Regional State Prosecutor’s Office, and then appointed as Head of Amhara National Regional State Anti-Corruption Office and served for 3 years.Mr. Ali has shown unprecedented performance in his career and hence he was appointed in the Federal Supreme Court and served at the Cassation Bench for over 10 years. He has published so many articles, provide several pieces of trainingd",
        contact: " ali@5alawoffice.com",
      },
      amare: {
        id: 2,
        img: require("../assets/Image/Amare.jpg"),
        name: "Amare Ashenafi",
        desc: "Founder and Partner of 5A, Amare earned his law degree (LLB) from Bahir Dar University, his LLM from Mekelle University in Tax and Investment Law, and two years post-graduate certificate from Federal Judges and Prosecutors Training Center. In his stay in Bahir Dar University, he was Student`s Union President and Ethiopian Universities President for more than three years.He worked as a District Prosecutor, Appellate Court Presiding Judge and President, Court Manager in Federal First Instance and Supreme Court of Ethiopia before founding 5A. With over 12 years of administrative and legal experience, he has advised government, national and multinational companies on reorganization, legal drafting, and investment issues.He presides as a judge in arbitration and advice clients on court cases. He has also lectured law at Saint Merry University on a part-time basis.",
        contact: "  amare@5alawoffice.com",
      },
      alemu: {
        id: 3,
        img: require("../assets/Image/Alemu.jpg"),
        name: "Alemu Korme",
        desc: "Founder and Partner of 5A, Alemu earned his law degree (LLB) from Addis Ababa University, his MBA from Lead Star University in collaboration with Ashland University, and a two years post-graduate certificate from Federal Judges and Prosecutors Training Center.He worked as an Assistant judge in Oromiya Supreme Court, First Instance and Appellate Court Judge, and Ethiopian Federal Revenue Authority Legal Expert before founding 5A. With over 12 years of legal experience, he has advised national and multinational companies on corporate and investment issues. He represents clients in arbitration and court cases. He has also lectured law at Rift Valley University on a part-time basis.",
        contact: " Alemu@5alawoffice.com",
      },
      almaw: {
        id: 4,
        img: require("../assets/Image/Almaw.jpg"),
        name: "Almaw Wolie",
        desc: "Founder and Partner of 5A, Almaw has received his Bachelor of Laws /LL. B/ from Addis Ababa University in July 2000 and his Master of Laws /LL.M/ in Constitutional and Public law from the same University in July 2007. He served for over 19.6 years in Ethiopian Judiciary.From this extensive judicial service, he had served as a High Court Judge for about 3 years and 4years as a judge of Amhara National Regional State Supreme Court. For the last 12 years, he had served as a judge at the apex of the Ethiopian Judiciary- Federal Supreme Court.From these Twelve Years of service, he served for about 9 months on the appellate bench and about 11 years and 3 months in the cassation division with not less than five judges. He served in the cassation division with not less than five judges as a judge and Presiding judge.",
        contact: "Almaw@5alawoffice.com",
      },

      ashenafi: {
        id: 5,
        img: require("../assets/Image/Ashenafi.jpg"),
        name: "Ashenafi Yirga",
        desc: "Founder and Partner of 5A, A graduate of the Law School of Bahir Dar University as an outstanding student, Ashenafi heads the Litigation Section in 5A. He has over 12 years of experience as a judge in the Amhara State Supreme Court and Federal High Court of Ethiopia.",
        contact: "Ashenafi@5alawoffice.com",
      },
      mesnbet: {
        id: 6,
        img: require("../assets/Image/mesnbet.jpg"),
        name: "DR.Mesnbet Assefa",
        desc: "Mesenbet earned his LL.B from Bahir Dar University in 2006 and graduated with distinction. He further pursued his graduate education and studied his LL.M in 2008 at the University of Pretoria in South Africa. He received his Ph.D. at the National University of Ireland Galway (NUIG) in 2017.Mesenbet has extensive experience in international law, comparative constitutional law, criminal law, business law, and human rights. Mesenbet has published in numerous international and local journals. He has presented his research findings in numerous Universities including Yale School of Law, London School of Economics, and the University of Seville. His particular research interests include development, Security/counterterrorism, human rights, constitutional law, and freedom of expression.Mesenbet has served in numerous positions including as Head of the School of Law Addis Ababa University, Associate Dean for Graduate Studies of Addis Ababa University School of Law, and Director of Mekelle University Human Rights Centre. Mesenbet has also extensive experience in consulting governmental, inter-governmental, and non-governmental organizations at various levels. Currently, he also serves as a committee member in the National Legal Reform Council of Ethiopia.",
        contact: "mesenbet@5alawoffice.com",
      },
      hanna: {
        id: 7,
        img: require("../assets/Image/hanna.jpg"),
        name: "Hanna Yohannes",
        desc: "Hanna Yohannes is an assistant lawyer and office manager at 5A Jurists Consultancy Group. Hanna believes that excellence can be achieved through dedication, focus and hard work. Hanna earned her Bachelors of Law /LL.B./from Addis Ababa University. In her stay at Addis Ababa University, she was working on human right and participated women’s empowerment and leadership training at Addis Ababa University. She participate in a voluntary work on various organization like orphanage village and on elderly support. She also worked as a legal advisor in NGOs. and associate at #I CARE campaign.",
        contact: "hanna@5alawoffice.com",
      },
      linora: {
        id: 8,
        img: require("../assets/Image/linora.jpg"),
        name: "Linora Mohammed",
        desc: "Assistant Lawyer of 5A, Linora earned her law degree (LLB) from Adigrat University as an outstanding student. In her stay of Adigrat University, she was the founder and the vice president of the Human Rights and Justice Club. She has participated in the 2015 Human rights day Moot court competition by representing the Law School of Adigrat University, which was organized by the Ethiopian Human right commission Mekelle branch which was based on Human Trafficking. In addition to that, she has persistently taken part in volunteer service in the summer at Federal Attorney General as an assistant of the public prosecutor at women’s and children’s offices. Post-graduation she served as a lecturer in the Law school of Adigrat University on a full-time basis.  ",
        contact: "linora@5alawoffice.com",
      },

      showPopup: false,
    };
  },
  methods: {
    togglePopup(name) {
      switch (name) {
        case "ali":
          this.modalData = this.ali;
          break;
        case "amare":
          this.modalData = this.amare;
          break;
        case "alemu":
          this.modalData = this.alemu;
          break;
        case "almaw":
          this.modalData = this.almaw;
          break;
        case "ashenafi":
          this.modalData = this.ashenafi;
          break;
        case "mesnbet":
          this.modalData = this.mesnbet;
          break;
        case "hanna":
          this.modalData = this.hanna;
          break;
        case "linora":
          this.modalData = this.linora;
          break;
      }
      this.showPopup = !this.showPopup;
    },
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
    background: url("../assets/Image/teambg.JPG") rgba(3, 42, 86, 0.3) no-repeat;
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
  .stand {
    margin-top: 8rem;

    background: url("../assets/Image/city.jpg") no-repeat rgba(0, 0, 0, 0.49);

    background-position: center center;
    background-size: cover;
    background-blend-mode: overlay;
    background-attachment: fixed;
    .container {
      padding: 2.5rem 0 4rem;

      .stand-content {
        // max-width: 32.69rem;

        h1 {
          @extend .h2;
          color: #fff;
          margin-bottom: 1.69rem;
          text-align: center;
        }
        p {
          font-weight: normal;
          font-size: 1.13rem;
          line-height: 1.75rem;
          color: #fff;
          margin-bottom: 1.2rem;
          // max-width: 28.19rem;
          text-align: center;
        }
        .button {
          display: grid;
          place-content: center;
          a {
            @extend .text;
            color: #fff;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .stand {
      .container {
        .stand-content {
          margin-left: 3rem;
          margin-right: 3rem;
        }
      }
    }
  }
  @include responsive($lg) {
    .stand {
      margin: 7rem 0;
      background-attachment: none;
    }
  }
  @include responsive($xl) {
    .stand {
      margin-top: 10rem;
      .container {
        .stand-content {
          margin-left: 10rem;
          margin-right: 10rem;
          h1 {
            margin-top: 3rem;
          }
          p {
            margin-top: 3rem;
            font-size: 1.13rem;
            margin-bottom: 4rem;
          }
        }
      }
    }
  }
  .picture {
    margin-top: 8rem;
    // background: rgba(42, 46, 83, 0.25);
    .wrapper {
      position: relative;
      z-index: -1;
      .team-img {
        height: 20rem;
        width: 100%;
        object-fit: cover;
      }
      .team-decor {
        position: absolute;
        top: 0;
        right: 0;
        height: 20rem;
        opacity: 0.7;
      }
    }
  }
  @include responsive($md) {
    .picture {
      margin-top: 10rem;
      .wrapper {
        .team-img {
          height: 25rem;
        }
        .team-decor {
          height: 25rem;
        }
      }
    }
  }
  @include responsive($xl) {
    .picture {
      margin-top: 10rem;
      .wrapper {
        .team-img {
          height: 30rem;
        }
        .team-decor {
          height: 30rem;
        }
      }
    }
  }
  @include responsive($xxl) {
    .picture {
      .wrapper {
        .team-img {
          height: 35rem;
        }
        .team-decor {
          height: 35rem;
        }
      }
    }
  }

  .pop-up {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(1, 0, 19, 0.37);
    // display: none;
    display: grid;
    place-items: center;
    z-index: 99999;
    .inner {
      position: absolute;
      z-index: 999999999;
      // left: 60%;
      width: 22rem;
      background: #fff;
      border-radius: 10px;
      padding: 2rem;
      // position: relative;
      transition: left 0.3s linear;
      .close-modal-btn {
        position: absolute;
        right: 0.5rem;
        top: -1rem;
        width: 3rem;
        cursor: pointer;
      }

      .bio {
        display: grid;
        place-items: center;
        // margin-top: 1rem;
        .decor {
          position: absolute;
          z-index: 99;
          top: 0;
          left: 1rem;
          width: 8rem;
          margin-top: 1rem;
        }

        .indiv-img {
          width: 12rem;
          position: relative;
        }
        h4 {
          @extend .title;
          color: $A-darkerblue;
          margin-top: 1rem;
          font-size: 1rem;
          font-weight: 600;
          text-align: center;
        }
        p {
          color: $A-darkerblue;
          @extend .text;
          font-size: 0.8rem;
          line-height: 1.13rem;
          margin-top: 0.5rem;
          text-align: center;
          a {
            color: $A-lightblue;
          }
        }
      }
    }
  }
  @include responsive($md) {
    .pop-up {
      .inner {
        width: 30rem;

        padding: 2rem;

        .bio {
          .decor {
            left: 2rem;
            width: 10rem;
            margin-top: 2rem;
          }

          .indiv-img {
            width: 15rem;
          }
          h4 {
            font-size: 1.3rem;
          }
        }
      }
    }
  }
  .topdecor {
    margin-top: 8rem;
    position: relative;

    .left {
      background: $A-darkerblue;
      width: 100%;
      height: 30vh;
      display: grid;
      place-items: center;
      .left-decor {
        position: absolute;
        left: 0;
        top: 0;
      }
      .edge-decor1 {
        top: -0.5rem;
        left: -0.5rem;
        position: absolute;
        z-index: 999;
      }
      h2 {
        @extend .title;
        color: $A-white;
        font-size: 1.5rem;
        font-weight: 600;
        text-align: center;
        z-index: 9999;
      }
    }
    .pass-decor {
      display: none;
      margin-top: -5rem;
      position: absolute;
      z-index: 999;
      opacity: 0.7;
    }
    .right {
      position: relative;
      .decor {
        height: 20rem;
        width: 100%;
        object-fit: cover;
      }
      .edge-decor {
        bottom: 0;
        right: -0.5rem;
        position: absolute;
        z-index: 999;
      }
    }
  }
  @include responsive($md) {
    .topdecor {
      display: flex;
      width: 100%;
      .left {
        height: 40vh;
      }
      .pass-decor {
        display: block;
        margin-top: 0rem;
        left: -4rem;
        bottom: 0;
        width: 40rem;
      }
      .right {
        .decor {
          height: 40vh;
        }
      }
    }
  }
  @include responsive($lg) {
    .topdecor {
      display: flex;
      .edge-decor1 {
        width: 8rem;
      }
      .left {
        width: 80%;
        height: 30vh;
      }
      .pass-decor {
        margin-top: 0rem;
        left: 3.3rem;
        bottom: 0;
        width: 50rem;
      }
      .right {
        .decor {
          height: 30vh;
        }
        .edge-decor {
          width: 8rem;
        }
      }
    }
  }
  @include responsive($xl) {
    .topdecor {
      .left {
        width: 45%;
        height: 40vh;
        h2 {
          font-size: 2rem;
        }
        .edge-decor1 {
          width: 10rem;
        }
      }
      .pass-decor {
        margin-left: 8rem;
        opacity: 0.5;
        bottom: 0;
      }
      .right {
        // background: url("../assets/Image/team2.JPG") rgba(3, 42, 86, 0.3);
        .decor {
          height: 40vh;
          width: 80rem;

          z-index: 9999;
        }
        .edge-decor {
          width: 10rem;
        }
      }
    }
  }
  @include responsive($xxl) {
    .topdecor {
      .left {
        width: 75%;
        height: 50vh;
        h2 {
          font-size: 2rem;
        }
      }
      .pass-decor {
        margin-left: 40rem;
      }
      .right {
        .decor {
          height: 50vh;
        }
      }
    }
  }
  .meet-team {
    // margin-top: 8rem;

    .container {
      h2 {
        @extend .title;
        color: $A-darkerblue;
        font-size: 1.5rem;
        font-weight: 600;
        text-align: center;
      }
      .team-wrapper {
        display: grid;
        place-items: center;
        .card {
          margin-top: 5rem;
          width: 16rem;
          cursor: pointer;

 &:hover{
   
          opacity: .7;
        }
          .indiv-pic {
            .indiv-img {
            }
            .bottom-decor {
              width: 13rem;
              height: 1rem;
              background: $A-lightblue;
     
            }
          }
                    &:hover .bottom-decor{
                  transform: translateX(3rem);
  
        }
          .name {
            h4 {
              @extend .title;
              color: $A-darkerblue;
              margin-top: 0.94rem;
              font-size: 1.5rem;
              text-align: left;
            }
            p {
              color: $A-darkerblue;
              @extend .text;
              font-size: 0.96rem;
              margin-top: 0.94rem;
              text-align: left;
            }
          }
        }
       
      }
    }
  }
  @include responsive($md) {
    .meet-team {
      .container {
        .team-wrapper {
          display: grid;
          grid-template-columns: 1fr 1fr;
          gap: 1rem;
          .card {
            .indiv-pic {
            }
          }
        }
      }
    }
  }
  @include responsive($lg) {
    .meet-team {
      .container {
        h2 {
          font-size: 2rem;
        }
        .team-wrapper {
          grid-template-columns: 1fr 1fr 1fr;

          .card {
            width: 19rem;

            .indiv-pic {
              width: 19rem;
            }
          }
        }
      }
    }
  }
  @include responsive($xl) {
    .meet-team {
      .container {
        h2 {
          font-size: 2.5rem;
        }
        .team-wrapper {
          gap: 1.5rem;

          .card {
            margin-top: 8rem;

            .indiv-pic {
              width: 19rem;
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