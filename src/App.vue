<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import FeatureChevron from './components/FeatureChevron.vue'
import QuoteCarousel from "./components/QuoteCarousel.vue";
import Options from './components/Options.vue'
import ProposeCard from './components/ProposeCard.vue'

import {
    menuItems,
    chevronData,
    optionsList,
    proposeData
} from './assets/mockData.js'

</script>

<template>
    <Header :menu="menuItems"/>

    <section class="feature">
        <div class="feature__content container container--pall">
            <div class="feature__intro">
                <h3>Enter your vehicle details to receive a free valuation.</h3>
                <p>
                    If your vehicle has <span class="text-bolder">less than 100,000 miles</span> enter your vehicle and contact details and we will contact you with a cash valuation within 24 hours.
                </p>
            </div>
            <div class="feature__intro">
                <form class="get-started">
                    <div>
                        <input type="text" placeholder="ENTER REG" class="inp-place" style="width: 100%; padding: 10px; font-size: 16px;"/>
                    </div>
                    <div class="terms" style="display: flex; align-items: center; margin-top: 10px;">
                        <input type="checkbox" id="checkbox" style="width: 20px; height: 20px;"/>
                        <label for="checkbox" style="margin-left: 10px; font-size: 14px;">
                            I confirm that the vehicle I am enquiring about has less than 100,000 miles.
                        </label>
                    </div>
                    <div style="margin-top: 10px;">
                        <button type="button" style="padding: 10px 20px; font-size: 16px; background-color: #2d314d;">
                            Get Started
                            <img src="./assets/images/icon-get-started.svg" class="get-started-icon"/>
                        </button>
                    </div>
                </form>
            </div>
        </div>
    </section>

    <ProposeCard :data="proposeData"/>

    <section class="how-to">
        <div class="container container--pall">
            <div class="how-to-info">
                <h4>How it works</h4>
                <p>It's so easy to sell your car with CashForCars!</p>
            </div>
            <div class="how-to-features">
                <FeatureChevron v-for="item in chevronData" :chevron-data="item"/>
            </div>
        </div>
    </section>

    <section class="car-propose">
        <h4>Why choose CashForCars to sell your car?</h4>
        <div class="car-propose-flex">
            <div class="item propose-text">
                <p>Advertising your car for sale privately can be a costly, not to mention frustrating process which
                    is renowned for attracting time wasters.</p>

                <p>Using CashForCars eliminates the hassle of strangers visiting your home, the worry associated with them taking a test drive uninsured and guarantees
                    peace of mind by working with a reputable company.</p>

                <p>By dealing directly with CashForCars you also eliminate the worry of cheques bouncing and unsatisfied customers returning to your door.</p>

                <p>CashForCars is the quick, easy and efficient way to turn your car into cash for whatever reason.
                    If you are purchasing a replacement vehicle of a dealer, selling your car to CashForCars puts you
                    in the driving seat and you will be able to negotiate a much better deal.</p>
            </div>
            <div class="item propose-image">
                <img src="./assets/images/car-propose.png" alt="car_propose">
            </div>
        </div>
    </section>

    <Options :options="optionsList"/>

    <section class="car-deals">
        <div class="deals-flex">
            <div class="deal-item">
                <h3>Trade In</h3>
                <p>Don't let dealers give you less at trade-in, take a look at why
                    CashForCars is a great way to get more money for your car! There are many
                    great reasons to choose us over a standard dealer trade-in!</p>
            </div>
            <div class="deal-item">
                <h3>Sell On Your Own</h3>
                <p>Selling a car on your own can be unpredictable and stressful, with CashForCars
                    you can sell your car as soon as you're ready. Check out why we're better than
                    selling it yourself!</p>
            </div>
        </div>
    </section>

    <section class="car-feedbacks">
        <div class="feedback-flex">
            <div class="item-feedback">
                <h3>What our customers <br> have been saying</h3>
            </div>
            <QuoteCarousel/>
        </div>
    </section>

    <section class="valuation">
        <div class="valuation-flex">
            <div class="valuation-item">
                <p>Receive your free valuation now</p>
                <button type="button">
                    Get Started
                    <img src="./assets/images/icon-get-started.svg" class="get-started-icon"/>
                </button>
            </div>
        </div>
    </section>
    <Footer :menu="menuItems"/>
</template>
