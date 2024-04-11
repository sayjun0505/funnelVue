<template>
  <div class="w-full">
    <!-- Team memners section -->
    <section id="hero" class="w-full pb-24">
      <BaseSection>
        <div class="col-span-12 lg:col-span-6 mt-12 xl:mt-10 space-y-4 sm:space-y-6 px-6 text-center sm:text-left">
          <h1 data-aos="fade-right" data-aos-once="true"
            class="text-[2.5rem] sm:text-5xl xl:text-6xl font-bold leading-tight capitalize sm:pr-8 xl:pr-10">
            Best way to <span class="text-header-gradient">manage your</span> projects
          </h1>
          <p data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="paragraph hidden sm:block">
            Get an all out tool to enhance your project management experience at the lowest price!
          </p>
          <div data-aos="fade-up" data-aos-once="true" data-aos-delay="700"
            class="flex flex-col sm:flex-row space-y-4 sm:space-y-0 sm:space-x-4 mt-2">
            <BaseButton
              class="max-w-full px-8 py-4 bg-gradient-to-r from-[#468ef9] to-[#0c66ee] border border-[#0c66ee] text-white">
              Subscribe Now
            </BaseButton>
          </div>
          <p data-aos="fade-down" data-aos-once="true" data-aos-delay="300" class="paragraph hidden sm:block">
            <span class="text-blue-600">50% OFF</span> FOR THIS MONTH
          </p>
        </div>
        <div class="hidden sm:block col-span-12 lg:col-span-6">

          <div class="w-full">
            <img data-aos="fade-up" data-aos-once="true" :src="require('~/assets/img/team_member.png')" class="-mt-4"
              alt="" />
          </div>
        </div>
        <img data-aos="fade-up" data-aos-delay="300" :src="require('~/assets/img/pattern/ellipse-1.png')"
          class="hidden sm:block absolute bottom-12 xl:bottom-16 left-4 xl:left-0 w-6" />
        <img data-aos="fade-up" data-aos-delay="300" :src="require('~/assets/img/pattern/ellipse-2.png')"
          class="hidden sm:block absolute top-4 sm:top-10 right-64 sm:right-96 xl:right-[32rem] w-6" />
        <img data-aos="fade-up" data-aos-delay="300" :src="require('~/assets/img/pattern/ellipse-3.png')"
          class="hidden sm:block absolute bottom-56 right-24 w-6" />
        <img data-aos="fade-up" data-aos-delay="300" :src="require('~/assets/img/pattern/star.png')"
          class="hidden sm:block absolute top-20 sm:top-28 right-16 lg:right-0 lg:left-[30rem] w-8" />
      </BaseSection>
    </section>

    <!-- Crypto statistic section -->
    <section
    class="max-w-screen-xl mx-2 sm:mx-auto px-4 sm:px-6 lg:px-0 py-6 pb-20 sm:py-8     ">
    <h1 data-aos="fade-right" data-aos-once="true"
      class="text-[2.5rem] sm:text-4xl xl:text-5xl font-bold leading-tight capitalize sm:pr-8 xl:pr-10 flex justify-center">
      Elevate Your <span class="text-blue-600 mx-3"> Business Work Processr </span> Easily
    </h1>
      <div class="w-full flex flex-col lg:flex-row items-center justify-center bg-white rounded-[2.25rem] sm:rounded-xl  shadow-lg sm:shadow-md mt-12">
        <LandingCryptoStatistic data-aos="fade-up" title="Project Management"
          description="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque"
          :datasets="trendings" class="xl:border-r border-gray-200 lg:px-8 py-8" />
        <LandingCryptoStatistic data-aos="fade-up" data-aos-delay="150" title="Meetings"
          description="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque"
          :datasets="topGainers" class="xl:border-r border-gray-200 lg:px-8" />
        <LandingCryptoStatistic data-aos="fade-up" data-aos-delay="300" title="Onboarding"
          description="Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque"
          :datasets="recents" class="lg:px-8" />
      </div>
    </section>

    <!-- Buy and trade section -->
    <section class="w-full my-24">
      <BaseSection>
        <LandingBuyTradeImage class="sm:hidden mb-8" />
        <div data-aos="fade-right" class="col-span-12 lg:col-span-6 mt-4 xl:mt-20 space-y-6 px-4">
          <h2 class="text-4xl font-semibold sm:pr-8 xl:pr-12">
            Use Powerful <br class="hidden sm:block" />
            Integration With SoftRex
          </h2>
          <p class="paragraph">
            Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa.
            Cum sociis natoque
          </p>
          <div class="space-y-6 lg:pr-12">
            <BaseButton class="w-full px-5 py-4 bg-blue-gradient text-white text-base font-medium"> Subscribe Now for
              Only $9 </BaseButton>
          </div>
        </div>
        <LandingBuyTradeImage data-aos="fade-left" class="hidden sm:block" />
      </BaseSection>
    </section>

    <!-- Partners section -->
    <section class="bg-partner relative max-w-full sm:mx-6 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full px-6 sm:px-0 py-16 flex flex-col items-center justify-center space-y-4 text-center">
        <h3 data-aos="flip-down" class="text-2xl text-neutral-800 font-semibold">Frequently asked questions</h3>
        <div data-aos="fade-up" class="flex flex-wrap items-center justify-center">
          <LandingPartnerImage v-for="query in queries" :key="query.title" :query="query" />
        </div>
      </div>
    </section>

    <!-- Industry-leading security section -->

    <section class="w-full my-24">
      <div data-aos="fade-left"
        class="grid justify-items-center col-span-12 lg:col-span-5 space-y-8 sm:space-y-6 mt-8 px-8">
        <h1 data-aos="fade-right" data-aos-once="true" class="font-bold leading-tight capitalize text-4xl">
          A Tool You <span class="text-blue-600">Can't Miss Out</span> On
        </h1>
        <p class="w-1/2 text-center">Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula
          eget dolor. Aenean massa. Cum
          sociis natoque</p>
      </div>
      <div data-aos="fade-right" class="grid justify-items-center flex-col col-span-12 lg:col-span-6 mt-12">
        <img :src="require('~/assets/img/youtube.png')" class="w-2/3" alt="" />
      </div>
    </section>

    <!-- Getting started section -->
    <section class="bg-trading-tools relative max-w-full sm:mx-4 xl:mx-10 my-24 shadow sm:rounded-2xl overflow-hidden">
      <div class="w-full py-16 flex flex-col items-center">
        <h2 data-aos="flip-down" class="text-3xl sm:text-4xl font-semibold text-center">
          Used by over 990+ companies in different countries
        </h2>
        <div data-aos="fade-up"
          class="relative w-full flex flex-col lg:flex-row items-center justify-between space-y-12 lg:space-y-0 px-4 xl:px-10 mt-16 sm:mt-8">
          <LandingStep v-for="step in steps" :key="step.title" :step="step" />
        </div>
      </div>
    </section>

    <!-- FAQ section -->

    <section class="w-full my-24 footer-back text-white py-24">
      <div class="flex justify-center">
        <h2 class="text-4xl sm:text-4xl font-semibold mb-10 sm:mb-6 ">Get started with ProRex</h2>
      </div>
      <div class="w-full flex flex-col lg:flex-row mt-12">
        <div class="w-full lg:w-1/3 mt-6 lg:mt-0 overflow-hidden space-y-6" v-bind="$attrs">
          <div class="w-full flex justify-center">
            <div v-for="data in datasets" :key="data.id" class="border-b border-gray-200">
              <img :src="require(`~/assets/img/crypto-icon/${data.logo}`)" alt=""
                class="bg-blue-600 w-20 h-20 p-5 rounded-3xl mr-3" />
            </div>
            <CheckCircleIcon :size="20" class="text-white flex justify-center items-center" />
            <h1 class="text-2xl text-center">Planning and scheduling</h1>
          </div>
        </div>
        <div class="w-full lg:w-1/3 mt-6 lg:mt-0 overflow-hidden space-y-6" v-bind="$attrs">
          <div class="w-full flex justify-center">
            <div v-for="data in datasets" :key="data.id" class="border-b border-gray-200">
              <img :src="require(`~/assets/img/crypto-icon/${data.logo}`)" alt=""
                class="bg-blue-600 w-20 h-20 p-5 rounded-3xl mr-3" />
            </div>
            <CheckCircleIcon :size="20" class="text-white flex justify-center items-center" />
            <h1 class="text-2xl text-center">Team collaboration</h1>
          </div>
        </div>
        <div class="w-full lg:w-1/3 mt-6 lg:mt-0 overflow-hidden space-y-6" v-bind="$attrs">
          <div class="w-full flex justify-center">
            <div v-for="data in datasets" :key="data.id" class="border-b border-gray-200">
              <img :src="require(`~/assets/img/crypto-icon/${data.logo}`)" alt=""
                class="bg-blue-600 w-20 h-20 p-5 rounded-3xl mr-3" />
            </div>
            <CheckCircleIcon :size="20" class="text-white flex justify-center items-center" />
            <h1 class="text-2xl text-center">Time tracking.</h1>
          </div>
        </div>
      </div>
      <div class="flex justify-center mt-16">
        <BaseButton class="px-5 py-4 bg-white text-blue-600 text-base font-medium "> Subscribe Now for
          Only $9
        </BaseButton>
      </div>
    </section>

    <div class="w-full my-10 flex justify-center">
      <a v-smooth-scroll data-aos="flip-down" data-aos-delay="150" href="#navbar"
        class="px-6 py-3 flex items-center space-x-2 bg-[#FAFAFA] hover:bg-gray-100 hover:shadow-md border border-[#DDDDDD] rounded-md text-gray-700">
        <span>Back to top</span>
        <ArrowUpIcon :size="20" />
      </a>
    </div>
  </div>
</template>

<script>
import aosMixin from '@/mixins/aos'
export default {
  name: 'IndexPage',
  mixins: [aosMixin],
  data() {
    return {
      selected: 0,
      dropdownConcurency: false,
      dropdownCrypto: false,
      currencySelected: {
        img: 'country-icon/eng.png',
        name: 'USD',
      },
      currencies: [
        {
          img: 'country-icon/eng.png',
          name: 'USD',
        },
      ],
      cryptoSelected: {
        img: 'crypto-icon/bitcoin.png',
        name: 'BTC',
      },
      cryptocurrencies: [
        {
          img: 'crypto-icon/bitcoin.png',
          name: 'BTC',
        },
      ],
      trendings: [
        {
          id: 1,
          name: 'Bitcoin',
          price: 43180.13,
          logo: 'project.png',
          increase: true,
          data: [40, 35, 60, 75, 60, 75, 50],
        }
      ],
      topGainers: [
        {
          id: 1,
          name: 'PAPPAY',
          price: 0.00374,
          logo: 'meeting.png',
          increase: true,
          data: [30, 50, 45, 60, 70, 40, 45],
        }
      ],
      recents: [
        {
          id: 1,
          name: 'MetaCraft',
          price: 0.0608,
          logo: 'onboarding.png',
          increase: false,
          data: [40, 50, 45, 60, 35, 40, 45],
        }
      ],
      steps: [
        {
          img: 'user1.png',
          title: 'Jhonathon Doe',
          description:
            'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis',
        },
        {
          img: 'user2.png',
          title: 'Jhonathon Doe',
          description:
            'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis',
        },
        {
          img: 'user3.png',
          title: 'Jhonathon Doe',
          description:
            'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis',
        },
        {
          img: 'user4.png',
          title: 'Jhonathon Doe',
          description:
            'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis',
        },
      ],
      queries: [
        {
          title: 'Is there a free version of SoftRex?',
          description: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis'
        },
        {
          title: 'How to upgrade to ultimate pro?',
          description: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis'
        },
        {
          title: 'Set permissions and admin controls',
          description: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis'
        },
        {
          title: 'How to start this tool?',
          description: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis'
        },
        {
          title: 'What is the refund policy?',
          description: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis'
        },
        {
          title: 'How to Integrate with SoftRex?',
          description: 'Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis'
        },
      ]
    }
  },
}
</script>
<style scoped>
.text-header-gradient {
  background: rgb(57, 132, 244);
  background: linear-gradient(169.4deg, #3984f4 -6.01%, #0cd3ff 36.87%, #2f7cf0 78.04%, #0e65e8 103.77%);
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.bg-partner {
  background: url('../assets/img/partner/background.png');
  background-size: cover;
  background-position: center;
}

.bg-trading-tools {
  background: url('../assets/img/bg-trading-tools.webp');
  background-size: cover;
  background-position: center;
}

.max-h-0 {
  max-height: 0;
}

.footer-back {
  background: url('../assets/img/footer_back.png') no-repeat;
  background-size: cover;
}
</style>
