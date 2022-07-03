<script setup>
import ContactCardVue from "./components/ContactCard.vue";
import IntroVue from "./components/Intro.vue";
import ExperienceVue from "./components/Experience.vue";
import EducationVue from "./components/Education.vue";
</script>

<template>
  <main>
    <ContactCardVue :contact="contact" />
    <IntroVue />
    <ExperienceVue :jobs="jobs" />
    <EducationVue />
  </main>
</template>

<script>
export default {
  data() {
    return {
      contact: [],
      jobs: [],
    };
  },
  created() {
    (this.contact = [
      {
        name: "Liam Cullen",
        details: {
          Phone: "0400 685 718",
          Email: "liamtc@icloud.com",
        },
      },
    ]),
      (this.jobs = [
        {
          position: "Marketing Web Designer",
          company: "Kogan.com",
          startDate: "Jan 2022",
          endDate: "Present",
          description: [
            "Use HTML, CSS and Javascript to build all custom web pages from scratch including promotions, brand pages and buying guides. Regularly review customer journeys to further enhance user experience across the site. Use React to programatically create motion graphics, fetching data from the site API.",
            "Build and maintain websites for brand verticals, including Kogan Internet and Insurance. Set up a structured Wordpress backend for easy team maintenance.",
          ],
          achievements: [
            "Designed crucial customer touch points including Order Confirmation & Customer Dashboard.",
            "Created branded email templates for all customer communication across five brands.",
            "Improved SEO and accessibility by building live web content in place of static images, and transitioning Size Charts from graphics to styled HTML tables.",
          ],
          skills: [
            "HTML",
            "CSS + SCSS",
            "Javascript",
            "Python",
            "React",
            "LiquidMarkup",
            "Photoshop",
            "Illustrator",
            "After Effects",
            "CSM",
            "SEO",
          ],
          logo: "kogan-logo.webp",
          include: true,
        },
        {
          position: "Marketing Content Coordinator",
          company: "Kogan.com",
          startDate: "Mar 2021",
          endDate: "Jan 2022",
          description: [
            "Created and maintained website content to maximise SEO and customer engagement. Reviewed product listings, categories and navigation to best showcase the product range. Built product collections and discounts for promotions and EDMs.",
          ],
          achievements: [
            "Leveraged Python to automate repetitive tasks.",
            "Created Photoshop scripts and actions to improve team efficiency.",
          ],
          skills: [
            "Photoshop",
            "Illustrator",
            "Python",
            "Graphic Design",
            "CSM",
            "SEO",
            "Push Notifications",
          ],
          logo: "kogan-logo.webp",
          include: true,
        },
        {
          position: "Customer Service Representative",
          company: "Kogan",
          startDate: "Jan 2021",
          endDate: "Mar 2021",
          description: [
            "Communicated effectively with customers to resolve enquiries regarding products, ordering and delivery. Worked closely with purchasing and logistics departments as well as delivery partners to provide fast and accurate information. ",
          ],
          achievements: [
            "Created Zendesk macros to improve ticket response time.",
          ],
          skills: [
            "SAP",
            "Communication",
            "Negotiation",
            "Customer Relations",
            "User Experience",
            "Communication",
          ],
          logo: "kogan-logo.webp",
          include: true,
        },
        {
          position: "Finishing Artist",
          company: "Wellcom Worldwide",
          startDate: "Jul 2019",
          endDate: "Mar 2020",
          description: [
            "Worked in a studio environment with talent, stylists and photographers to deliver high quality imagery for digital and print channels. Integrated within client offices to provide graphic design support, from motion graphics to form design. ",
          ],
          achievements: [
            "Retouched photography for national print and digital campaigns for clients including David Jones, Coles and Target.",
            "Built customer forms for national banks and superannuation providers including ANZ and AMP.",
          ],
          skills: [
            "Photoshop",
            "Illustrator",
            "After Effects",
            "Lightroom",
            "Bridge",
          ],
          logo: "wellcom-logo.png",
          include: true,
        },
        {
          position: "Graphic Design Internship",
          company: "Papas Shorts (Berlin)",
          startDate: "Jan 2019",
          endDate: "Mar 2019",
          description: [
            "Assumed ownership of many aspects of the brand's design, including packaging and web design to instill a consistent image and message. Photographed and Filmed content for product listings, EDMs and social media",
          ],
          achievements: [
            "Designed packaging for all customer orders.",
            "Created business cards for company founders.",
            "Initiated a Marketing strategy and brand style guide.",
          ],
          skills: [
            "Photoshop",
            "Illustrator",
            "InDesign",
            "Photography",
            "Cinematography",
            "HTML",
            "CSS",
            "Wordpress",
            "Packaging Design",
            "Brand Analysis",
          ],
          logo: "papas-shorts.webp",
          include: true,
        },
        {
          position: "Retail Operations Coordinator",
          company: "Myer",
          startDate: "Mar 2017",
          endDate: "Jul 2019",
          description: [
            "Monitored the operations of Myer's warehouses to ensure the fulfillment of online orders including shipping and in-store collection. Maintained stock inventory levels across a national network of stores. ",
          ],
          achievements: [
            "Refined and modernised processes for efficiency.",
            "Developed strong relationships with key stakeholders.",
          ],
          skills: ["Telecommunications", "Process Review", "Logistics"],
          logo: "myer-logo.svg",
          include: true,
        },
        {
          position: "Team Leader",
          company: "Myer",
          startDate: "Aug 2016",
          endDate: "Mar 2017",
          description: [
            "Managed a team of customer service staff to ensure a high level of consistent customer care was provided. Helped team members develop through training and feedback on KPIs. ",
          ],
          achievements: [
            "Produced a weekly social newsletter.",
            "Provided support through a challenging transitional period.",
          ],
          skills: [
            "Leadership",
            "Rostering",
            "Escalation Management",
            "Training",
          ],
          logo: "myer-logo.svg",
          include: true,
        },
        {
          position: "Customer Service Representative",
          company: "Myer",
          startDate: "Oct 2015",
          endDate: "Aug 2016",
          description: [
            "Answered customer enquiries relating to Myer’s loyalty program, online store and general customer service. Managed communication channels including Phone, Email and Social Media. ",
          ],
          achievements: [
            "Became a subject matter expert, assisting team members with internal software.",
          ],
          skills: [
            "IBM COM",
            "Communication",
            "Negotiation",
            "Customer Relations",
            "User Experience",
          ],
          logo: "myer-logo.svg",
          include: false,
        },
        {
          position: "Cook",
          company: "McDonalds",
          startDate: "Mar 2015",
          endDate: "Oct 2015",
          description: [
            "Prepared customer orders with a high focus on consistent quality. Prepared ingredients to ensure a smooth kitchen operation. ",
          ],
          achievements: [],
          skills: ["Time management", "communication"],
          logo: "mcdonalds-logo.svg",
          include: false,
        },
        {
          position: "Sales Representative",
          company: "Easy Being Green",
          startDate: "Jan 2015",
          endDate: "Mar 2015",
          description: [
            "Travelled across Melbourne offering customers energy saving products. Placed and managed orders for customers, liaising with a team of electricians. ",
          ],
          achievements: [],
          skills: ["Negotiation", "communication", "sales"],
          logo: "easy-being-green.png",
          include: false,
        },
        {
          position: "Kitchen Hand / Waiter",
          company: "A Bite to Eat",
          startDate: "May 2012",
          endDate: "Dec 2014",
          description: [
            "Maintained a clean and well prepared kitchen. Prepared and served meals and fresh beverages.",
          ],
          achievements: [
            "Added a virtual map to the store's EPOS system, allowing service staff to easily place orders for the correct tables.",
          ],
          skills: ["Time management", "communication", "EPOS"],
          logo: "a-bite-to-eat-logo.jpeg",
          include: false,
        },
      ]);
  },
};
</script>

<style>
@import "./assets/base.css";
@import "./assets/reset.css";
</style>
