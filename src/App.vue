<template>
  <div id="app">
    <AppHeader :linksArray="headerNavLinks" />
    <AppJumbo />
    <AppMain
      :staringCardsArray="startingCards"
      :aboutUsOptionsArray="aboutUsDetails"
      :thisCoursesData="aboutUsData"
      :thisFeaturedCourses="featuredCourses"
    />
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppJumbo from "./components/AppJumbo.vue";
import AppMain from "./components/AppMain.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppJumbo,
    AppMain,
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
    };
  },
};
</script>

<style lang="scss">
@import "./style/common.scss";
</style>
