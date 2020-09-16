<!DOCTYPE html>
<html lang="en">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" type="text/css" href="https://cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.css"/>
    <link href="https://fonts.googleapis.com/css?family=Open+Sans:400,700&display=swap" rel="stylesheet">

    <style>
        a,
        .header{
            color: #FFFFFF
        }
        .slick-dots li button:before,
        .slick-dots li.slick-active button:before {
            background-color: #FFFFFF;
        }
        @media screen and (min-width:725px) {
            .slick-list{
                background:#fff;height:350px;overflow:auto;overflow-x:hidden;
            }
        }
        body,
        html {
            height: 100%;
            width: 100%
        }
        body {
            font-family: 'Open Sans', sans-serif;
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
            margin: 0
        }
        a {
            font-weight: 700;
            text-decoration: none
        }
        .root {
            position: relative;
            padding: 16px 40px;
            max-width: 900px;
            background-color: #106582;
        }
        .container {
            color: #fff;
            text-align: center;
            width: 100%
        }
        .header {
            display: flex;
            flex-direction: column;
            align-items: center
        }
        .header__rating {
            display: flex;
            align-items: center
        }
        .header__stars {
            margin-right: 16px
        }
        .header__stars svg {
            background-color: #106582;
            border-radius: 4px;
            height: 24px;
            width: 24px
        }
        .header__stats {
            margin: 8px 0
        }
        .header__read-all {
            font-size: 1em
        }
        .slider-container {
            position: relative
        }
        .arrow {
            position: absolute;
            top: 50%;
            cursor: pointer
        }
        .arrow--left {
            left: -52px
        }
        .arrow--right {
            right: -52px
        }
        .arrow svg {
            width: 64px;
            height: 64px
        }
        .slider {
            margin: 16px 0 40px;
            background-color: #fff;
            box-shadow: 0 1px 3px 0 rgba(0, 0, 0, .2), 0 1px 1px 0 rgba(0, 0, 0, .14), 0 2px 1px -1px rgba(0, 0, 0, .12);
            border-radius: 4px;
            font-size: .8em;
            text-align: left;
            color: #000
        }
        .slider__no-reviews {
            display: flex;
            align-items: center;
            justify-content: center;
            min-height: 160px;
            height: 100%
        }
        .slide {
            padding: 16px
        }
        .slide:focus {
            outline: 0
        }
        .slide__title-container {
            margin-bottom: 24px
        }
        .slide__title-wrapper {
            display: flex;
            align-items: center;
            justify-content: space-between
        }
        .slide__title-stars {
            margin-top: 4px
        }
        .slide__title {
            margin: 0;
            font-size: 1.5em;
            color: #69ba00
        }
        .slide__answered-question {
            margin: 0 0 16px
        }
        .slide__question {
            margin: 0 0 8px
        }
        .slide__answer {
            margin: 0
        }
        .logo {
            display: block;
            width: 140px;
            margin: 0 auto
        }
        .logo__img {
            width: 100%
        }
        @media screen and (max-width:725px) {
            .slide__title-wrapper {
                align-items: flex-start;
                flex-direction: column
            }
        }
        @media screen and (max-width:575px) {
            .root {
                padding: 24px
            }
            .header__rating {
                flex-direction: column
            }
            .header__stars {
                margin-right: 0
            }
            .header__stars svg {
                width: 24px;
                height: 24px
            }
            .header__read-all {
                font-size: 1em
            }
            .arrow--left {
                display: none!important;
                left: -24px
            }
            .arrow--right {
                display: none!important;
                right: -24px
            }
        }
        .slick-loading .slick-list {
            background: #fff
        }
        .slick-dots {
            position: absolute;
            bottom: -32px;
            display: block;
            width: 100%;
            padding: 0;
            margin: 0;
            list-style: none;
            text-align: center
        }
        .slick-dots li {
            position: relative;
            display: inline-block;
            width: 20px;
            height: 16px;
            margin: 0 5px;
            padding: 0;
            cursor: pointer
        }
        .slick-dots li button {
            font-size: 0;
            line-height: 0;
            display: block;
            width: 8px;
            height: 8px;
            padding: 5px;
            cursor: pointer;
            color: transparent;
            border: 0;
            outline: 0;
            background: 0 0
        }
        .slick-dots li button:focus,
        .slick-dots li button:hover {
            outline: 0
        }
        .slick-dots li button:focus:before,
        .slick-dots li button:hover:before {
            opacity: 1
        }
        .slick-dots li button:before {
            display: block;
            width: 8px;
            height: 8px;
            content: '';
            opacity: .25;
            border-radius: 50%
        }
        .slick-dots li.slick-active button:before {
            opacity: .75
        }
        .badge {
            position: absolute;
            display: flex;
            align-items: center;
            top: 8px;
            left: 16px;
        }
        @media screen and (max-width:725px) {
            .badge {
                position: unset;
                justify-content: center;
                top: 0;
                left: 0;
            }
        }
        .badge__image {
            width: 32px;
        }
        .badge__text {
            margin-left: 8px;
            color: #FFFFFF;
            font-weight: 700;
        }
    </style>
</head>
<body>
<div class="root">
    <div class="container">
        <div class="header">
            <div class="header__rating">
                <div class="header__stars">

                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                            <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#FFFFFF" />
                            <path d="M0 0h24v24H0z" fill="none" />
                        </svg>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                            <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#FFFFFF" />
                            <path d="M0 0h24v24H0z" fill="none" />
                        </svg>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                            <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#FFFFFF" />
                            <path d="M0 0h24v24H0z" fill="none" />
                        </svg>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                            <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#FFFFFF" />
                            <path d="M0 0h24v24H0z" fill="none" />
                        </svg>
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                            <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#FFFFFF" />
                            <path d="M0 0h24v24H0z" fill="none" />
                        </svg>
                  </div>
                <p class="header__stats"><strong>23</strong> reviews | <strong>5</strong> Verified advisers</p>
            </div>
            <span class="header__read-all">Selection of recent reviews. <a href="https://vouchedfor.co.uk" target="_blank" rel="noreferrer noopener">Read all Reviews</a></span>
        </div>
            <div class="slider-container">
                <div class="slider" id="slick">

                        <div class="slide">
                            <div class="slide__title-container">
                                <div class="slide__title-wrapper">
                                    <h2 class="slide__title">
                                        Review from verified client for Sarah Roberts
                                    </h2>
                                    <div class="slide__title-stars">

                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>

                                    </div>
                                </div>
                                <span>September 2020</span>
                            </div>

                                <div class="slide__answered-question">
                                  <h3 class="slide__question">
                                    What were the circumstances that caused you to look for a financial adviser?
                                  </h3>
                                  <p class="slide__answer">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                                  </p>
                                  <br>
                                  <h3 class="slide__question">
                                    How did Sarah Roberts help you?
                                  </h3>
                                  <p class="slide__answer">
                                    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
                                  </p>
                                  <br>
                                  <h3 class="slide__question">
                                    Have you seen the outcome you were hoping for?
                                  </h3>
                                  <p class="slide__answer">
                                    Yes, absolutely!
                                  </p>
                                </div>

                        </div>
                        <div class="slide">
                            <div class="slide__title-container">
                                <div class="slide__title-wrapper">
                                    <h2 class="slide__title">
                                        Review from verified client for Bob Smith
                                    </h2>
                                    <div class="slide__title-stars">

                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>

                                    </div>
                                </div>
                                <span>September 2020</span>
                            </div>

                                <div class="slide__answered-question">
                                    <h3 class="slide__question">
                                      What were the circumstances that caused you to look for a financial adviser?
                                    </h3>
                                    <p class="slide__answer">
                                      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                                    </p>
                                    <br>
                                    <h3 class="slide__question">
                                      How did Bob Smith help you?
                                    </h3>
                                    <p class="slide__answer">
                                      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                                    </p>
                                    <br>
                                    <h3 class="slide__question">
                                      Have you seen the outcome you were hoping for?
                                    </h3>
                                    <p class="slide__answer">
                                      Yes, absolutely!
                                    </p>
                                </div>


                        </div>
                        <div class="slide">
                            <div class="slide__title-container">
                                <div class="slide__title-wrapper">
                                    <h2 class="slide__title">
                                        Review from verified client for Rachel White
                                    </h2>
                                    <div class="slide__title-stars">

                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>
                                            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24"><path d="M0 0h24v24H0z" fill="none" />
                                                <path d="M12 17.27L18.18 21l-1.64-7.03L22 9.24l-7.19-.61L12 2 9.19 8.63 2 9.24l5.46 4.73L5.82 21z" fill="#0099bc" />
                                                <path d="M0 0h24v24H0z" fill="none" />
                                            </svg>

                                    </div>
                                </div>
                                <span>September 2020</span>
                            </div>

                                <div class="slide__answered-question">
                                    <h3 class="slide__question">
                                      What were the circumstances that caused you to look for a financial adviser?
                                    </h3>
                                    <p class="slide__answer">
                                      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                                    </p>
                                    <br>
                                    <h3 class="slide__question">
                                      How did Rachel White help you?
                                    </h3>
                                    <p class="slide__answer">
                                      Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
                                    </p>
                                    <br>
                                    <h3 class="slide__question">
                                      Have you seen the outcome you were hoping for?
                                    </h3>
                                    <p class="slide__answer">
                                      Yes, very happy
                                    </p>
                                </div>


                        </div>

                </div>
                <div class="arrow arrow--left">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                        <path d="M15.41 7.41L14 6l-6 6 6 6 1.41-1.41L10.83 12z" fill="#FFFFFF"/>
                        <path d="M0 0h24v24H0z" fill="none"/>
                    </svg>
                </div>
                <div class="arrow arrow--right">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                        <path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z" fill="#FFFFFF" />
                        <path d="M0 0h24v24H0z" fill="none"/>
                    </svg>
                </div>
            </div>
        <a class="logo" href="https://vouchedfor.co.uk" target="_blank" rel="noreferrer noopener">
            <img
                class="logo__img"
                src="https://assets.vouchedfor.co.uk/img/widget/powered-by-white.png"
                alt="Powered by VouchedFor"
            >
        </a>
    </div>
</div>
<script src="https://code.jquery.com/jquery-3.4.1.slim.min.js" integrity="sha256-pasqAKBDmFT4eHoN2ndd6lN370kFiGUFyTiUHWhU7k8=" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/slick-carousel@1.8.1/slick/slick.min.js"></script>
<script>
    (function ($) {
        $(document).ready(function(){
            $('#slick').slick({
                dots: true,
                arrows: true,
                prevArrow: $('.arrow--left'),
                nextArrow: $('.arrow--right'),
            });
        });
    })(jQuery);
</script>
</body>
</html>
