<template>
  <div id="app">
    <AppHeader :linksArray="headerNavLinks" />
    <AppJumbo />
    <AppMain
      :staringCardsArray="startingCards"
      :aboutUsOptionsArray="aboutUsDetails"
      :thisCoursesData="aboutUsData"
      :thisFeaturedCourses="featuredCourses"
      :thisEventsArray="eventsArray"
      :thisTestimonialsArray="testimonialsArray"
    />
    <AppFooter :thisFooterData="footerData" :theseSocial="socialIcons" />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbo from "./components/AppJumbo.vue";
import AppMain from "./components/AppMain.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbo,
    AppMain,
    AppFooter,
  },
  data() {
    return {
      headerNavLinks: ["Home", "Pages", "Courses", "Features", "Blog", "Shop"],
      startingCards: [
        {
          image: "01",
          title: "Idea Discussion",
          text: "Get teamed up with the specialists who work and teach coding for years at famous university",
        },
        {
          image: "02",
          title: "Web Development",
          text: "Learn to start building a webpage from scratch. You decide your own pace, course and speed",
        },
        {
          image: "03",
          title: "System Administration",
          text: "Learners are encouraged to study the mechanism and structure of system administration",
        },
        {
          image: "04",
          title: "Graphic Design",
          text: "Have a passion for graphic and arts? Show your talents with confidence and self-assertiveness",
        },
      ],
      aboutUsDetails: [
        {
          id: 0,
          title: "Multiple Platforms Supported for Teaching & Studing",
          content:
            "MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access in our knowledge base from any device",
        },
        {
          id: 1,
          title: "Multiple Course Participation at the Same Time",
          content:
            "MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access in our knowledge base from any device",
        },
        {
          id: 2,
          title: "Track Study Progress & Deliver Prompt Feedback",
          content:
            "MaxCoach supports the act of teaching and learning on multiple platforms like online or offline via material downloads. We know things aren't supposed to be devoured in a short time, you can always access in our knowledge base from any device",
        },
      ],
      aboutUsData: [
        {
          number: "1.926",
          label: "FINISHED SESSIONS",
        },
        {
          number: "3.092+",
          label: "ENROLLED LEANERS",
        },
        {
          number: "200",
          label: "ONLINE INSTRUCTORS",
        },
        {
          number: "100%",
          label: "SATISFACTION RATE",
        },
      ],
      featuredCourses: [
        {
          image: "02",
          name: "Blanche Fields",
          avatar: "73ee246daf47502812ccefc84bf02898",
          price: "40.00",
          text: "Leaning to Write as a Professional Author",
          statics: {
            lessons: "20",
            students: "50",
          },
        },
        {
          image: "hd-03",
          name: "Maggie Strickland",
          avatar: "d0d504142acfde820eef2f11feea6253",
          price: "Free",
          text: "Customer-centric Info-tech Stategies",
          statics: {
            lessons: "24",
            students: "769",
          },
        },
        {
          image: "hd-04",
          name: "Maggie Strickland",
          avatar: "d0d504142acfde820eef2f11feea6253",
          price: "19.00",
          text: "Open Programming Courses for Everyone: Python",
          statics: {
            lessons: "17",
            students: "62",
          },
        },
        {
          image: "hd-06",
          name: "Blanche Fields",
          avatar: "73ee246daf47502812ccefc84bf02898",
          price: "26.00",
          text: "Academic Listening and Note-taking",
          statics: {
            lessons: "14",
            students: "67",
          },
        },
        {
          image: "featured-image-01",
          name: "Blanche Fields",
          avatar: "73ee246daf47502812ccefc84bf02898",
          price: "39.00",
          text: "Master jQuery in a Short Period of Time",
          statics: {
            lessons: "6",
            students: "51",
          },
        },
        {
          image: "hd-05",
          name: "Blanche Fields",
          avatar: "73ee246daf47502812ccefc84bf02898",
          price: "59.00",
          text: "Introduction to Javascript for beginners",
          statics: {
            lessons: "14",
            students: "76",
          },
        },
      ],
      eventsArray: [
        {
          title: "Storytelling Workshop",
          location: "Texas, US",
          date: {
            day: "22",
            month: "November",
          },
        },
        {
          title: "Painting Art Contest 2020",
          location: "New York, US",
          date: {
            day: "10",
            month: "October",
          },
        },
        {
          title: "International Art Fair 2020",
          location: "Hamburg, Germany",
          date: {
            day: "23",
            month: "November",
          },
        },
        {
          title: "Street Performance: Call for Artist",
          location: "Illinois, US",
          date: {
            day: "15",
            month: "December",
          },
        },
        {
          title: "Consumer Food Safety Education Conference",
          location: "Illinois, US",
          date: {
            day: "22",
            month: "July",
          },
        },
        {
          title: "How meditation improve your mental health?",
          location: "Dubai",
          date: {
            day: "12",
            month: "August",
          },
        },
      ],
      testimonialsArray: [
        [
          {
            name: "Mina Hollace",
            occupation: "Freelancer",
            text: "I am free to learn at my own pace, follow my own schedule and choose the subject you like. Great study portal for people like me.",
            image: "02",
          },
          {
            name: "Madley Pondor",
            occupation: "IT Specialist",
            text: "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
            image: "04",
          },
          {
            name: "Luvic Dubble",
            occupation: "Private Tutor",
            text: "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.",
            image: "01",
          },
        ],
        [
          {
            name: "John Smith",
            occupation: "Freelancer",
            text: "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
            image: "03",
          },
          {
            name: "Luvic Dubble",
            occupation: "Private Tutor",
            text: "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.",
            image: "01",
          },
          {
            name: "Mina Hollace",
            occupation: "Freelancer",
            text: "I am free to learn at my own pace, follow my own schedule and choose the subject you like. Great study portal for people like me.",
            image: "02",
          },
        ],
        [
          {
            name: "Mina Hollace",
            occupation: "Freelancer",
            text: "I am free to learn at my own pace, follow my own schedule and choose the subject you like. Great study portal for people like me.",
            image: "02",
          },
          {
            name: "Madley Pondor",
            occupation: "IT Specialist",
            text: "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
            image: "04",
          },
          {
            name: "Luvic Dubble",
            occupation: "Private Tutor",
            text: "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.",
            image: "01",
          },
        ],
        [
          {
            name: "Luvic Dubble",
            occupation: "Private Tutor",
            text: "I am free to learn at my own pace, follow my own schedule and choose the subject you like. Great study portal for people like me.",
            image: "01",
          },
          {
            name: "John Smith",
            occupation: "Freelancer",
            text: "MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.",
            image: "03",
          },
          {
            name: "Madley Pondor",
            occupation: "IT Specialist",
            text: "I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation.",
            image: "04",
          },
        ],
      ],
      footerData: [
        {
          title: "Address",
          links: [
            "382 NE 191st ST # 87394 Miami, FL 33179-3899",
            "+1 (305) 547-9909 (9am - 5am EST, Monday - Friday)",
            "support@maxcoach.com",
          ],
        },
        {
          title: "Explore",
          links: [
            "Start here",
            "Blog",
            "About us",
            "Success story",
            "Courses",
            "Contact Us",
          ],
        },
        {
          title: "Information",
          links: [
            "Membership",
            "Purhase guide",
            "Privacy policy",
            "Terms of services",
          ],
        },
      ],
      socialIcons: ["facebook-square", "twitter", "instagram", "linkedin"],
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
