<script setup lang="ts">
import { Accordion, AccordionContent, AccordionItem, AccordionTrigger } from '@/components/ui/accordion'
import accordionItems from './Q_A_items.json'


</script>

<template>
  <div class="full-page-container">
    <div class="faq-section">
      <h1>SIK SORULAN SORULAR</h1>
    </div>
    <div class="background-blur"></div>
    <Accordion type="single" class="w-full" collapsible :default-value="'item-1'">
      <AccordionItem v-for="item in accordionItems" :key="item.value" :value="item.value">
        <AccordionTrigger>{{ item.title }}</AccordionTrigger>
        <AccordionContent>
          {{ item.answer }}
        </AccordionContent>
      </AccordionItem>
    </Accordion>
    <div class="about-section">

      <h3>Bizi takip edin!</h3>
      <div class="social-links">
        <a href="https://www.instagram.com/chain.academy/" target="_blank" rel="noopener noreferrer">
          <img src="./assets/iglogo.png"  />
        </a>
        <a href="https://twitter.com/chain_academyy" target="_blank" rel="noopener noreferrer">
          <img src="./assets/xlogo.png" />
        </a>
      </div>
    </div>

  </div>
</template>


<style>
.full-page-container {
  width: 100%;
  height: 100%;
  position: relative;

}


.background-blur {
  position: absolute;
  width: 100%;
  height: 100%;
  background-image: url('./assets/backimg.jpg');
  background-size: cover;
  filter: blur(20px);
  /* Adjust the blur amount as needed for readability */
  z-index: -1;
}

.faq-section {
  font-size: 30px;
  padding-bottom: 40px;
  /* Adjust the padding-bottom as needed */
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.about-section {
  padding-top: 10%;
  text-align: center;
}

.social-links {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 20px;
}

.social-links a {
  display: inline-block;
  text-decoration: none;
  color: #000; /* Adjust the color as needed */
  margin: 0 10px;
}

.social-links a:hover {
  text-decoration: underline;
}

</style>