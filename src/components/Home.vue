<template>
    <div class="clearfix home">
        <div class="seaweed-right">
            <img class="right-seaweed" src="../assets/title-card-seaweed-right.png" />
        </div>
        <div class="seaweed-left">
            <img class="left-seaweed" src="../assets/title-card-seaweed-left.png" />
        </div>
        <v-container fluid class="home-content">
            <app-logo></app-logo>
            <v-row>
                <v-col xs12 sm12 md12 lg12>
                    <div class="home-title">
                        <p id="vthacksTitle">{{ msg }}</p>
                        <p id="vthacksNum">IV</p>
                    </div>
                    <div id="vthacksDate">
                        February 12th, 2017
                    </div>
                    <router-link style='text-decoration: none' to='/register'>
                        <v-btn :ripple="{class: 'teal--text'}" class="vt-submit-btn" round>Register</v-btn>
                    </router-link>
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script>
    import Logo from '../components/Logo'

    export default {
        name: 'home',
        components: {
            appLogo: Logo
        },
        data () {
            return {
                msg: 'VTHACKS'
            }
        }
    }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    h1, h2 {
        font-weight: normal;
    }
    ul {
        list-style-type: none;
        padding: 0;
    }
    .landing-background-img {
        position: relative;
    }
    li {
        display: inline-block;
        margin: 0 10px;
    }

    a {
        color: #42b983;
    }
    .home-content {
        text-align: center;
        padding: 10vh;
    }
    @media screen and (max-width: 576px) {
        .home-content {
            padding: 0;
            width: none;
        }
    }
    .seaweed-right {
        width: 30vh;
        float: right;
    }
    img.right-seaweed {
        position: fixed;
        height: 100vh;
        width: 40vh;
    }
    img.left-seaweed {
        position: fixed;
        height: 100vh;
        width: 30vh;
    }
    @media screen and (max-width: 1180px) {
        .seaweed-right, .seaweed-left{
            display: none;
        }
    }
    @media (min-width: 0px) and (max-width: 740px) {
        .home-title {
            font-size: 10rem;
        }
        #vthacksTitle {
            margin: 0;
            display: block!important;
        }
        #vthacksNum {
            margin-top: -3vh;
            display: block!important;
        }
    }
    @media (min-width: 0px) and (max-width: 450px) {
        .home-content {
            margin: 12vh 0 0 0;
        }
    }
    @media (width: 320px) {
        .home-content {
            margin-top: 12vh;
        }
        #vthacksDate {
            margin: 0 0 10px 0;
        }
    }
    .home-title {
        font-size: 8vh;
    }
    #vthacksTitle {
        background: -webkit-linear-gradient(#084b56, #2ab3a5);
        -webkit-background-clip: text;
        -webkit-text-fill-color: rgba(0, 0, 0, 0.08);
        font-weight: 900;
        color: #00897b;
        display: inline;
    }
    #vthacksNum {
        font-weight: 100!important;
        color: #ffffff;
        display: inline-block;
    }
    #vthacksDate {
        margin: 1vh 0 4vh 0;
        color: #ffffff;
        font-size: 3vh;
        font-weight: 600;
    }
</style>
