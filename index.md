<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>2048</title>

  <link href="style/main.css" rel="stylesheet" type="text/css">
  <link rel="shortcut icon" href="favicon.ico">
  <link rel="apple-touch-icon" href="meta/apple-touch-icon.png">
  <link rel="apple-touch-startup-image" href="meta/apple-touch-startup-image-640x1096.png" media="(device-width: 320px) and (device-height: 568px) and (-webkit-device-pixel-ratio: 2)"> <!-- iPhone 5+ -->
  <link rel="apple-touch-startup-image" href="meta/apple-touch-startup-image-640x920.png"  media="(device-width: 320px) and (device-height: 480px) and (-webkit-device-pixel-ratio: 2)"> <!-- iPhone, retina -->
  <meta name="apple-mobile-web-app-capable" content="yes">
  <meta name="apple-mobile-web-app-status-bar-style" content="black">

  <meta name="HandheldFriendly" content="True">
  <meta name="MobileOptimized" content="320">
  <meta name="viewport" content="width=device-width, target-densitydpi=160dpi, initial-scale=1.0, maximum-scale=1, user-scalable=no, minimal-ui">
</head>
<body>
  <div class="container">
    <div class="heading">
      <h1 class="title">2048</h1>
      <div class="scores-container">
        <div class="score-container">0</div>
        <div class="best-container">0</div>
      </div>
    </div>

    <div class="above-game">
      <p class="game-intro">Join the numbers and get to the <strong>2048 tile!</strong></p>
      <a class="restart-button">New Game</a>
    </div>

    <div class="game-container">
      <div class="game-message">
        <p></p>
        <div class="lower">
	        <a class="keep-playing-button">Keep going</a>
          <a class="retry-button">Try again</a>
        </div>
      </div>

      <div class="grid-container">
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
        <div class="grid-row">
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
          <div class="grid-cell"></div>
        </div>
      </div>

      <div class="tile-container">

      </div>
    </div>

    <p class="game-explanation">
      <strong class="important">How to play:</strong> Use your <strong>arrow keys</strong> to move the tiles. When two tiles with the same number touch, they <strong>merge into one!</strong>
    </p>
  </div>

  <script src="js/bind_polyfill.js"></script>@import url(fonts/clear-sans.css);
html, body {
  margin: 0;
  padding: 0;
  background: url('../udacity/green.png');
  background-position: center center;
  background-repeat: no-repeat;
  color: #06010A;
  font-family: "Clear Sans", "Helvetica Neue", Arial, sans-serif;
  font-size: 18px; }


body {
  margin: 80px 0;
  background-color: 090203 }

.heading:after {
  content: "";
  display: block;
  clear: both; }

h1.title {
  font-size: 80px;
  font-weight: bold;
  margin: 0;
  display: block;
  float: left; }

@-webkit-keyframes move-up {
  0% {
    top: 25px;
    opacity: 1; }

  100% {
    top: -50px;
    opacity: 0; } }
@-moz-keyframes move-up {
  0% {
    top: 25px;
    opacity: 1; }

  100% {
    top: -50px;
    opacity: 0; } }
@keyframes move-up {
  0% {
    top: 25px;
    opacity: 1; }

  100% {
    top: -50px;
    opacity: 0; } }
.scores-container {
  float: right;
  text-align: right; }

.score-container, .best-container {
  position: relative;
  display: inline-block;
  background: #2C92DE;
  padding: 15px 25px;
  font-size: 25px;
  height: 25px;
  line-height: 47px;
  font-weight: bold;
  border-radius: 3px;
  color: white;
  margin-top: 8px;
  text-align: center; }
  .score-container:after, .best-container:after {
    position: absolute;
    width: 100%;
    top: 10px;
    left: 0;
    text-transform: uppercase;
    font-size: 13px;
    line-height: 13px;
    text-align: center;
    color: #9F41D5; }
  .score-container .score-addition, .best-container .score-addition {
    position: absolute;
    right: 30px;
    color: red;
    font-size: 25px;
    line-height: 25px;
    font-weight: bold;
    color: rgba(119, 110, 101, 0.9);
    z-index: 100;
    -webkit-animation: move-up 600ms ease-in;
    -moz-animation: move-up 600ms ease-in;
    animation: move-up 600ms ease-in;
    -webkit-animation-fill-mode: both;
    -moz-animation-fill-mode: both;
    animation-fill-mode: both; }

.score-container:after {
  content: "Score"; }

.best-container:after {
  content: "Best"; }

p {
  margin-top: 0;
  margin-bottom: 10px;
  line-height: 1.65; }

a {
  color: #2CDE37;
  font-weight: bold;
  text-decoration: underline;
  cursor: pointer; }

strong.important {
  text-transform: uppercase; }

hr {
  border: none;
  border-bottom: 1px solid #FF005D;
  margin-top: 20px;
  margin-bottom: 30px; }

.container {
  width: 500px;
  margin: 0 auto; }

@-webkit-keyframes fade-in {
  0% {
    opacity: 0; }

  100% {
    opacity: 1; } }
@-moz-keyframes fade-in {
  0% {
    opacity: 0; }

  100% {
    opacity: 1; } }
@keyframes fade-in {
  0% {
    opacity: 0; }

  100% {
    opacity: 1; } }
.game-container {
  margin-top: 40px;
  position: relative;
  padding: 15px;
  cursor: default;
  -webkit-touch-callout: none;
  -ms-touch-callout: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  -ms-touch-action: none;
  touch-action: none;
  background: #2C92DE;
  border-radius: 6px;
  width: 500px;
  height: 500px;
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box; }
  .game-container .game-message {
    display: none;
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background: rgba(150, 150, 150, 0.83);
    z-index: 100;
    text-align: center;
    -webkit-animation: fade-in 800ms ease 1200ms;
    -moz-animation: fade-in 800ms ease 1200ms;
    animation: fade-in 800ms ease 1200ms;
    -webkit-animation-fill-mode: both;
    -moz-animation-fill-mode: both;
    animation-fill-mode: both; }
    .game-container .game-message p {
      font-size: 60px;
      font-weight: bold;
      height: 60px;
      line-height: 60px;
      margin-top: 222px; }
    .game-container .game-message .lower {
      display: block;
      margin-top: 59px; }
    .game-container .game-message a {
      display: inline-block;
      background: #2C92DE;
      border-radius: 3px;
      padding: 0 20px;
      text-decoration: none;
      color: #f9f6f2;
      height: 40px;
      line-height: 42px;
      margin-left: 9px; }
      .game-container .game-message a.keep-playing-button {
        display: none; }
    .game-container .game-message.game-won {
      background: rgba(237, 194, 46, 0.5);
      color: #2C92DE; }
      .game-container .game-message.game-won a.keep-playing-button {
        display: inline-block; }
    .game-container .game-message.game-won, .game-container .game-message.game-over {
      display: block; }

.grid-container {
  position: absolute;
  z-index: 1; }

.grid-row {
  margin-bottom: 15px; }
  .grid-row:last-child {
    margin-bottom: 0; }
  .grid-row:after {
    content: "";
    display: block;
    clear: both; }

.grid-cell {
  width: 106.25px;
  height: 106.25px;
  margin-right: 15px;
  float: left;
  border-radius: 3px;
  background: rgba(238, 228, 218, 0.35); }
  .grid-cell:last-child {
    margin-right: 0; }

.tile-container {
  position: absolute;
  z-index: 2; }

.tile, .tile .tile-inner {
  width: 107px;
  height: 107px;
  line-height: 107px; }
.tile.tile-position-1-1 {
  -webkit-transform: translate(0px, 0px);
  -moz-transform: translate(0px, 0px);
  -ms-transform: translate(0px, 0px);
  transform: translate(0px, 0px); }
.tile.tile-position-1-2 {
  -webkit-transform: translate(0px, 121px);
  -moz-transform: translate(0px, 121px);
  -ms-transform: translate(0px, 121px);
  transform: translate(0px, 121px); }
.tile.tile-position-1-3 {
  -webkit-transform: translate(0px, 242px);
  -moz-transform: translate(0px, 242px);
  -ms-transform: translate(0px, 242px);
  transform: translate(0px, 242px); }
.tile.tile-position-1-4 {
  -webkit-transform: translate(0px, 363px);
  -moz-transform: translate(0px, 363px);
  -ms-transform: translate(0px, 363px);
  transform: translate(0px, 363px); }
.tile.tile-position-2-1 {
  -webkit-transform: translate(121px, 0px);
  -moz-transform: translate(121px, 0px);
  -ms-transform: translate(121px, 0px);
  transform: translate(121px, 0px); }
.tile.tile-position-2-2 {
  -webkit-transform: translate(121px, 121px);
  -moz-transform: translate(121px, 121px);
  -ms-transform: translate(121px, 121px);
  transform: translate(121px, 121px); }
.tile.tile-position-2-3 {
  -webkit-transform: translate(121px, 242px);
  -moz-transform: translate(121px, 242px);
  -ms-transform: translate(121px, 242px);
  transform: translate(121px, 242px); }
.tile.tile-position-2-4 {
  -webkit-transform: translate(121px, 363px);
  -moz-transform: translate(121px, 363px);
  -ms-transform: translate(121px, 363px);
  transform: translate(121px, 363px); }
.tile.tile-position-3-1 {
  -webkit-transform: translate(242px, 0px);
  -moz-transform: translate(242px, 0px);
  -ms-transform: translate(242px, 0px);
  transform: translate(242px, 0px); }
.tile.tile-position-3-2 {
  -webkit-transform: translate(242px, 121px);
  -moz-transform: translate(242px, 121px);
  -ms-transform: translate(242px, 121px);
  transform: translate(242px, 121px); }
.tile.tile-position-3-3 {
  -webkit-transform: translate(242px, 242px);
  -moz-transform: translate(242px, 242px);
  -ms-transform: translate(242px, 242px);
  transform: translate(242px, 242px); }
.tile.tile-position-3-4 {
  -webkit-transform: translate(242px, 363px);
  -moz-transform: translate(242px, 363px);
  -ms-transform: translate(242px, 363px);
  transform: translate(242px, 363px); }
.tile.tile-position-4-1 {
  -webkit-transform: translate(363px, 0px);
  -moz-transform: translate(363px, 0px);
  -ms-transform: translate(363px, 0px);
  transform: translate(363px, 0px); }
.tile.tile-position-4-2 {
  -webkit-transform: translate(363px, 121px);
  -moz-transform: translate(363px, 121px);
  -ms-transform: translate(363px, 121px);
  transform: translate(363px, 121px); }
.tile.tile-position-4-3 {
  -webkit-transform: translate(363px, 242px);
  -moz-transform: translate(363px, 242px);
  -ms-transform: translate(363px, 242px);
  transform: translate(363px, 242px); }
.tile.tile-position-4-4 {
  -webkit-transform: translate(363px, 363px);
  -moz-transform: translate(363px, 363px);
  -ms-transform: translate(363px, 363px);
  transform: translate(363px, 363px); }

.tile {
  position: absolute;
  -webkit-transition: 100ms ease-in-out;
  -moz-transition: 100ms ease-in-out;
  transition: 100ms ease-in-out;
  -webkit-transition-property: -webkit-transform;
  -moz-transition-property: -moz-transform;
  transition-property: transform; }
  .tile .tile-inner {
    border-radius: 3px;
    background: #eee4da;
    text-align: center;
    font-weight: bold;
    z-index: 10;
    font-size: 55px; }
  .tile.tile-2 .tile-inner {
    background: url('../udacity/2.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0), inset 0 0 0 1px rgba(255, 255, 255, 0); }
  .tile.tile-4 .tile-inner {
    background: url('../udacity/4.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0), inset 0 0 0 1px rgba(255, 255, 255, 0); }
  .tile.tile-8 .tile-inner {
    background: url('../udacity/8.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    font-weight: medium;
    font-size: 11px;
  }
  .tile.tile-16 .tile-inner {
    background: url('../udacity/16.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    font-weight: medium;
    font-size: 10px;
  }
  .tile.tile-32 .tile-inner {
    background: url('../udacity/32.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    font-size: 14px;
  }
  .tile.tile-64 .tile-inner {
    background: url('../udacity/64.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    font-size: 14px;

  }
  .tile.tile-128 .tile-inner {
    font-weight: medium;
    background: url('../udacity/128.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0.2381), inset 0 0 0 1px rgba(255, 255, 255, 0.14286);
    font-size: 12px; }
    @media screen and (max-width: 520px) {
      .tile.tile-128 .tile-inner {
        font-size: 12px; } }
  .tile.tile-256 .tile-inner {
    background: url('../udacity/256.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0.31746), inset 0 0 0 1px rgba(255, 255, 255, 0.19048);
    font-size: 14px; }
    @media screen and (max-width: 520px) {
      .tile.tile-256 .tile-inner {
        font-size: 16px; } }
  .tile.tile-512 .tile-inner {
    background: url('../udacity/512.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0.39683), inset 0 0 0 1px rgba(255, 255, 255, 0.2381);
    font-size: 13px; }
    @media screen and (max-width: 520px) {
      .tile.tile-512 .tile-inner {
        font-size: 13px; } }
  .tile.tile-1024 .tile-inner {
    background: url('../udacity/1024.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0.47619), inset 0 0 0 1px rgba(255, 255, 255, 0.28571);
    font-size: 10px; }
    @media screen and (max-width: 520px) {
      .tile.tile-1024 .tile-inner {
        font-size: 10px; } }
  .tile.tile-2048 .tile-inner {
    background: url('../udacity/2048.png');
    background-size: 100%;
    color: rgba(0,0,0,0);
    box-shadow: 0 0 30px 10px rgba(243, 215, 116, 0.55556), inset 0 0 0 1px rgba(255, 255, 255, 0.33333);
    font-size: 10px; }
    @media screen and (max-width: 520px) {
      .tile.tile-2048 .tile-inner {
        font-size: 10px; } }
  .tile.tile-super .tile-inner {
    color: #f9f6f2;
    background: #3c3a32;
    font-weight: medium;
    font-size: 12px; }
    @media screen and (max-width: 520px) {
      .tile.tile-super .tile-inner {
        font-size: 10px; } }

@-webkit-keyframes appear {
  0% {
    opacity: 0;
    -webkit-transform: scale(0);
    -moz-transform: scale(0);
    -ms-transform: scale(0);
    transform: scale(0); }

  100% {
    opacity: 1;
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1); } }
@-moz-keyframes appear {
  0% {
    opacity: 0;
    -webkit-transform: scale(0);
    -moz-transform: scale(0);
    -ms-transform: scale(0);
    transform: scale(0); }

  100% {
    opacity: 1;
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1); } }
@keyframes appear {
  0% {
    opacity: 0;
    -webkit-transform: scale(0);
    -moz-transform: scale(0);
    -ms-transform: scale(0);
    transform: scale(0); }

  100% {
    opacity: 1;
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1); } }
.tile-new .tile-inner {
  -webkit-animation: appear 200ms ease 100ms;
  -moz-animation: appear 200ms ease 100ms;
  animation: appear 200ms ease 100ms;
  -webkit-animation-fill-mode: backwards;
  -moz-animation-fill-mode: backwards;
  animation-fill-mode: backwards; }

@-webkit-keyframes pop {
  0% {
    -webkit-transform: scale(0);
    -moz-transform: scale(0);
    -ms-transform: scale(0);
    transform: scale(0); }

  50% {
    -webkit-transform: scale(1.2);
    -moz-transform: scale(1.2);
    -ms-transform: scale(1.2);
    transform: scale(1.2); }

  100% {
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1); } }
@-moz-keyframes pop {
  0% {
    -webkit-transform: scale(0);
    -moz-transform: scale(0);
    -ms-transform: scale(0);
    transform: scale(0); }

  50% {
    -webkit-transform: scale(1.2);
    -moz-transform: scale(1.2);
    -ms-transform: scale(1.2);
    transform: scale(1.2); }

  100% {
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1); } }
@keyframes pop {
  0% {
    -webkit-transform: scale(0);
    -moz-transform: scale(0);
    -ms-transform: scale(0);
    transform: scale(0); }

  50% {
    -webkit-transform: scale(1.2);
    -moz-transform: scale(1.2);
    -ms-transform: scale(1.2);
    transform: scale(1.2); }

  100% {
    -webkit-transform: scale(1);
    -moz-transform: scale(1);
    -ms-transform: scale(1);
    transform: scale(1); } }
.tile-merged .tile-inner {
  z-index: 20;
  -webkit-animation: pop 200ms ease 100ms;
  -moz-animation: pop 200ms ease 100ms;
  animation: pop 200ms ease 100ms;
  -webkit-animation-fill-mode: backwards;
  -moz-animation-fill-mode: backwards;
  animation-fill-mode: backwards; }

.above-game:after {
  content: "";
  display: block;
  clear: both; }

.game-intro {
  float: left;
  line-height: 42px;
  margin-bottom: 0; }

.restart-button {
  display: inline-block;
  background: #A350CA;
  border-radius: 3px;
  padding: 0 20px;
  text-decoration: none;
  color: #f9f6f2;
  height: 40px;
  line-height: 42px;
  display: block;
  text-align: center;
  float: right; }

.game-explanation {
  margin-top: 50px; }

@media screen and (max-width: 520px) {
  html, body {
    font-size: 15px; }

  body {
    margin: 20px 0;
    padding: 0 20px; }

  h1.title {
    font-size: 27px;
    margin-top: 15px; }

  .container {
    width: 280px;
    margin: 0 auto; }

  .score-container, .best-container {
    margin-top: 0;
    padding: 15px 10px;
    min-width: 40px; }

  .heading {
    margin-bottom: 10px; }

  .game-intro {
    width: 55%;
    display: block;
    box-sizing: border-box;
    line-height: 1.65; }

  .restart-button {
    width: 42%;
    padding: 0;
    display: block;
    box-sizing: border-box;
    margin-top: 2px; }

  .game-container {
    margin-top: 17px;
    position: relative;
    padding: 10px;
    cursor: default;
    -webkit-touch-callout: none;
    -ms-touch-callout: none;
    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;
    -ms-touch-action: none;
    touch-action: none;
    background: #4FEC43;
    border-radius: 6px;
    width: 280px;
    height: 280px;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box; }
    .game-container .game-message {
      display: none;
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background: rgba(238, 228, 218, 0.5);
      z-index: 100;
      text-align: center;
      -webkit-animation: fade-in 800ms ease 1200ms;
      -moz-animation: fade-in 800ms ease 1200ms;
      animation: fade-in 800ms ease 1200ms;
      -webkit-animation-fill-mode: both;
      -moz-animation-fill-mode: both;
      animation-fill-mode: both; }
      .game-container .game-message p {
        font-size: 60px;
        font-weight: bold;
        height: 60px;
        line-height: 60px;
        margin-top: 222px; }
      .game-container .game-message .lower {
        display: block;
        margin-top: 59px; }
      .game-container .game-message a {
        display: inline-block;
        background: #4FEC43;
        border-radius: 3px;
        padding: 0 20px;
        text-decoration: none;
        color: #f9f6f2;
        height: 40px;
        line-height: 42px;
        margin-left: 9px; }
        .game-container .game-message a.keep-playing-button {
          display: none; }
      .game-container .game-message.game-won {
        background: rgba(237, 194, 46, 0.5);
        color: #130619; }
        .game-container .game-message.game-won a.keep-playing-button {
          display: inline-block; }
      .game-container .game-message.game-won, .game-container .game-message.game-over {
        display: block; }

  .grid-container {
    position: absolute;
    z-index: 1; }

  .grid-row {
    margin-bottom: 10px; }
    .grid-row:last-child {
      margin-bottom: 0; }
    .grid-row:after {
      content: "";
      display: block;
      clear: both; }

  .grid-cell {
    width: 57.5px;
    height: 57.5px;
    margin-right: 10px;
    float: left;
    border-radius: 3px;
    background: rgba(238, 228, 218, 0.35); }
    .grid-cell:last-child {
      margin-right: 0; }

  .tile-container {
    position: absolute;
    z-index: 2; }

  .tile, .tile .tile-inner {
    width: 58px;
    height: 58px;
    line-height: 58px; }
  .tile.tile-position-1-1 {
    -webkit-transform: translate(0px, 0px);
    -moz-transform: translate(0px, 0px);
    -ms-transform: translate(0px, 0px);
    transform: translate(0px, 0px); }
  .tile.tile-position-1-2 {
    -webkit-transform: translate(0px, 67px);
    -moz-transform: translate(0px, 67px);
    -ms-transform: translate(0px, 67px);
    transform: translate(0px, 67px); }
  .tile.tile-position-1-3 {
    -webkit-transform: translate(0px, 135px);
    -moz-transform: translate(0px, 135px);
    -ms-transform: translate(0px, 135px);
    transform: translate(0px, 135px); }
  .tile.tile-position-1-4 {
    -webkit-transform: translate(0px, 202px);
    -moz-transform: translate(0px, 202px);
    -ms-transform: translate(0px, 202px);
    transform: translate(0px, 202px); }
  .tile.tile-position-2-1 {
    -webkit-transform: translate(67px, 0px);
    -moz-transform: translate(67px, 0px);
    -ms-transform: translate(67px, 0px);
    transform: translate(67px, 0px); }
  .tile.tile-position-2-2 {
    -webkit-transform: translate(67px, 67px);
    -moz-transform: translate(67px, 67px);
    -ms-transform: translate(67px, 67px);
    transform: translate(67px, 67px); }
  .tile.tile-position-2-3 {
    -webkit-transform: translate(67px, 135px);
    -moz-transform: translate(67px, 135px);
    -ms-transform: translate(67px, 135px);
    transform: translate(67px, 135px); }
  .tile.tile-position-2-4 {
    -webkit-transform: translate(67px, 202px);
    -moz-transform: translate(67px, 202px);
    -ms-transform: translate(67px, 202px);
    transform: translate(67px, 202px); }
  .tile.tile-position-3-1 {
    -webkit-transform: translate(135px, 0px);
    -moz-transform: translate(135px, 0px);
    -ms-transform: translate(135px, 0px);
    transform: translate(135px, 0px); }
  .tile.tile-position-3-2 {
    -webkit-transform: translate(135px, 67px);
    -moz-transform: translate(135px, 67px);
    -ms-transform: translate(135px, 67px);
    transform: translate(135px, 67px); }
  .tile.tile-position-3-3 {
    -webkit-transform: translate(135px, 135px);
    -moz-transform: translate(135px, 135px);
    -ms-transform: translate(135px, 135px);
    transform: translate(135px, 135px); }
  .tile.tile-position-3-4 {
    -webkit-transform: translate(135px, 202px);
    -moz-transform: translate(135px, 202px);
    -ms-transform: translate(135px, 202px);
    transform: translate(135px, 202px); }
  .tile.tile-position-4-1 {
    -webkit-transform: translate(202px, 0px);
    -moz-transform: translate(202px, 0px);
    -ms-transform: translate(202px, 0px);
    transform: translate(202px, 0px); }
  .tile.tile-position-4-2 {
    -webkit-transform: translate(202px, 67px);
    -moz-transform: translate(202px, 67px);
    -ms-transform: translate(202px, 67px);
    transform: translate(202px, 67px); }
  .tile.tile-position-4-3 {
    -webkit-transform: translate(202px, 135px);
    -moz-transform: translate(202px, 135px);
    -ms-transform: translate(202px, 135px);
    transform: translate(202px, 135px); }
  .tile.tile-position-4-4 {
    -webkit-transform: translate(202px, 202px);
    -moz-transform: translate(202px, 202px);
    -ms-transform: translate(202px, 202px);
    transform: translate(202px, 202px); }

  .tile .tile-inner {
    font-size: 35px; }

  .game-message p {
    font-size: 30px !important;
    height: 30px !important;
    line-height: 30px !important;
    margin-top: 90px !important; }
  .game-message .lower {// Exponent
// From: https://github.com/Team-Sass/Sassy-math/blob/master/sass/math.scss#L36

@function exponent($base, $exponent) {
  // reset value
  $value: $base;
  // positive intergers get multiplied
  @if $exponent > 1 {
    @for $i from 2 through $exponent {
      $value: $value * $base; } }
  // negitive intergers get divided. A number divided by itself is 1
  @if $exponent < 1 {
    @for $i from 0 through -$exponent {
      $value: $value / $base; } }
  // return the last value written
  @return $value;
}

@function pow($base, $exponent) {
  @return exponent($base, $exponent);
}

// Transition mixins
@mixin transition($args...) {
  -webkit-transition: $args;
  -moz-transition: $args;
  transition: $args;
}

@mixin transition-property($args...) {
  -webkit-transition-property: $args;
  -moz-transition-property: $args;
  transition-property: $args;
}

@mixin animation($args...) {
  -webkit-animation: $args;
  -moz-animation: $args;
  animation: $args;
}

@mixin animation-fill-mode($args...) {
  -webkit-animation-fill-mode: $args;
  -moz-animation-fill-mode: $args;
  animation-fill-mode: $args;
}

@mixin transform($args...) {
  -webkit-transform: $args;
  -moz-transform: $args;
  -ms-transform: $args;
  transform: $args;
}

// Keyframe animations
@mixin keyframes($animation-name) {
  @-webkit-keyframes $animation-name {
    @content;
  }
  @-moz-keyframes $animation-name {
    @content;
  }
  @keyframes $animation-name {
    @content;
  }
}

// Media queries
@mixin smaller($width) {
  @media screen and (max-width: $width) {
    @content;
  }
}

// Clearfix
@mixin clearfix {
  &:after {
    content: "";
    display: block;
    clear: both;
  }
}@import "helpers";
@import "fonts/clear-sans.css";

$field-width: 500px;
$grid-spacing: 15px;
$grid-row-cells: 4;
$tile-size: ($field-width - $grid-spacing * ($grid-row-cells + 1)) / $grid-row-cells;
$tile-border-radius: 3px;

$mobile-threshold: $field-width + 20px;

$text-color: #776E65;
$bright-text-color: #f9f6f2;

$tile-color: #eee4da;
$tile-gold-color: #edc22e;
$tile-gold-glow-color: lighten($tile-gold-color, 15%);

$game-container-margin-top: 40px;
$game-container-background: #bbada0;

$transition-speed: 100ms;

html, body {
  margin: 0;
  padding: 0;

  background: #faf8ef;
  color: $text-color;
  font-family: "Clear Sans", "Helvetica Neue", Arial, sans-serif;
  font-size: 18px;
}

body {
  margin: 80px 0;
}

.heading {
  @include clearfix;
}

h1.title {
  font-size: 80px;
  font-weight: bold;
  margin: 0;
  display: block;
  float: left;
}

@include keyframes(move-up) {
  0% {
    top: 25px;
    opacity: 1;
  }

  100% {
    top: -50px;
    opacity: 0;
  }
}

.scores-container {
  float: right;
  text-align: right;
}

.score-container, .best-container {
  $height: 25px;

  position: relative;
  display: inline-block;
  background: $game-container-background;
  padding: 15px 25px;
  font-size: $height;
  height: $height;
  line-height: $height + 22px;
  font-weight: bold;
  border-radius: 3px;
  color: white;
  margin-top: 8px;
  text-align: center;

  &:after {
    position: absolute;
    width: 100%;
    top: 10px;
    left: 0;
    text-transform: uppercase;
    font-size: 13px;
    line-height: 13px;
    text-align: center;
    color: $tile-color;
  }

  .score-addition {
    position: absolute;
    right: 30px;
    color: red;
    font-size: $height;
    line-height: $height;
    font-weight: bold;
    color: rgba($text-color, .9);
    z-index: 100;
    @include animation(move-up 600ms ease-in);
    @include animation-fill-mode(both);
  }
}

.score-container:after {
  content: "Score";
}

.best-container:after {
  content: "Best"
}

p {
  margin-top: 0;
  margin-bottom: 10px;
  line-height: 1.65;
}

a {
  color: $text-color;
  font-weight: bold;
  text-decoration: underline;
  cursor: pointer;
}

strong {
  &.important {
    text-transform: uppercase;
  }
}

hr {
  border: none;
  border-bottom: 1px solid lighten($text-color, 40%);
  margin-top: 20px;
  margin-bottom: 30px;
}

.container {
  width: $field-width;
  margin: 0 auto;
}

@include keyframes(fade-in) {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

// Styles for buttons
@mixin button {
  display: inline-block;
  background: darken($game-container-background, 20%);
  border-radius: 3px;
  padding: 0 20px;
  text-decoration: none;
  color: $bright-text-color;
  height: 40px;
  line-height: 42px;
}

// Game field mixin used to render CSS at different width
@mixin game-field {
  .game-container {
    margin-top: $game-container-margin-top;
    position: relative;
    padding: $grid-spacing;

    cursor: default;
    -webkit-touch-callout: none;
    -ms-touch-callout: none;

    -webkit-user-select: none;
    -moz-user-select: none;
    -ms-user-select: none;

    -ms-touch-action: none;
    touch-action: none;

    background: $game-container-background;
    border-radius: $tile-border-radius * 2;
    width: $field-width;
    height: $field-width;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;

    .game-message {
      display: none;

      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      background: rgba($tile-color, .5);
      z-index: 100;

      text-align: center;

      p {
        font-size: 60px;
        font-weight: bold;
        height: 60px;
        line-height: 60px;
        margin-top: 222px;
        // height: $field-width;
        // line-height: $field-width;
      }

      .lower {
        display: block;
        margin-top: 59px;
      }

      a {
        @include button;
        margin-left: 9px;
        // margin-top: 59px;

	&.keep-playing-button {
	  display: none;
	}
      }

      @include animation(fade-in 800ms ease $transition-speed * 12);
      @include animation-fill-mode(both);

      &.game-won {
        background: rgba($tile-gold-color, .5);
        color: $bright-text-color;

	a.keep-playing-button {
	  display: inline-block;
	}
      }

      &.game-won, &.game-over {
        display: block;
      }
    }
  }

  .grid-container {
    position: absolute;
    z-index: 1;
  }

  .grid-row {
    margin-bottom: $grid-spacing;

    &:last-child {
      margin-bottom: 0;
    }

    &:after {
      content: "";
      display: block;
      clear: both;
    }
  }

  .grid-cell {
    width: $tile-size;
    height: $tile-size;
    margin-right: $grid-spacing;
    float: left;

    border-radius: $tile-border-radius;

    background: rgba($tile-color, .35);

    &:last-child {
      margin-right: 0;
    }
  }

  .tile-container {
    position: absolute;
    z-index: 2;
  }

  .tile {
    &, .tile-inner {
      width: ceil($tile-size);
      height: ceil($tile-size);
      line-height: ceil($tile-size);
    }

    // Build position classes
    @for $x from 1 through $grid-row-cells {
      @for $y from 1 through $grid-row-cells {
        &.tile-position-#{$x}-#{$y} {
          $xPos: floor(($tile-size + $grid-spacing) * ($x - 1));
          $yPos: floor(($tile-size + $grid-spacing) * ($y - 1));
          @include transform(translate($xPos, $yPos));
        }
      }
    }
  }
}

// End of game-field mixin
@include game-field;

.tile {
  position: absolute; // Makes transforms relative to the top-left corner

  .tile-inner {
    border-radius: $tile-border-radius;

    background: $tile-color;
    text-align: center;
    font-weight: bold;
    z-index: 10;

    font-size: 55px;
  }

  // Movement transition
  @include transition($transition-speed ease-in-out);
  -webkit-transition-property: -webkit-transform;
  -moz-transition-property: -moz-transform;
  transition-property: transform;

  $base: 2;
  $exponent: 1;
  $limit: 11;

  // Colors for all 11 states, false = no special color
  $special-colors: false false, // 2
                   false false, // 4
                   #f78e48 true, // 8
                   #fc5e2e true, // 16
                   #ff3333 true, // 32
                   #ff0000 true, // 64
                   false true, // 128
                   false true, // 256
                   false true, // 512
                   false true, // 1024
                   false true; // 2048

  // Build tile colors
  @while $exponent <= $limit {
    $power: pow($base, $exponent);

    &.tile-#{$power} .tile-inner {
      // Calculate base background color
      $gold-percent: ($exponent - 1) / ($limit - 1) * 100;
      $mixed-background: mix($tile-gold-color, $tile-color, $gold-percent);

      $nth-color: nth($special-colors, $exponent);

      $special-background: nth($nth-color, 1);
      $bright-color: nth($nth-color, 2);

      @if $special-background {
        $mixed-background: mix($special-background, $mixed-background, 55%);
      }

      @if $bright-color {
        color: $bright-text-color;
      }

      // Set background
      background: $mixed-background;

      // Add glow
      $glow-opacity: max($exponent - 4, 0) / ($limit - 4);

      @if not $special-background {
        box-shadow: 0 0 30px 10px rgba($tile-gold-glow-color, $glow-opacity / 1.8),
                    inset 0 0 0 1px rgba(white, $glow-opacity / 3);
      }

      // Adjust font size for bigger numbers
      @if $power >= 100 and $power < 1000 {
        font-size: 45px;

        // Media queries placed here to avoid carrying over the rest of the logic
        @include smaller($mobile-threshold) {
          font-size: 25px;
        }
      } @else if $power >= 1000 {
        font-size: 35px;

        @include smaller($mobile-threshold) {
          font-size: 15px;
        }
      }
    }

    $exponent: $exponent + 1;
  }

  // Super tiles (above 2048)
  &.tile-super .tile-inner {
    color: $bright-text-color;
    background: mix(#333, $tile-gold-color, 95%);

    font-size: 30px;

    @include smaller($mobile-threshold) {
      font-size: 10px;
    }
  }
}

@include keyframes(appear) {
  0% {
    opacity: 0;
    @include transform(scale(0));
  }

  100% {
    opacity: 1;
    @include transform(scale(1));
  }
}

.tile-new .tile-inner {
  @include animation(appear 200ms ease $transition-speed);
  @include animation-fill-mode(backwards);
}

@include keyframes(pop) {
  0% {
    @include transform(scale(0));
  }

  50% {
    @include transform(scale(1.2));
  }

  100% {
    @include transform(scale(1));
  }
}

.tile-merged .tile-inner {
  z-index: 20;
  @include animation(pop 200ms ease $transition-speed);
  @include animation-fill-mode(backwards);
}

.above-game {
  @include clearfix;
}

.game-intro {
  float: left;
  line-height: 42px;
  margin-bottom: 0;
}

.restart-button {
  @include button;
  display: block;
  text-align: center;
  float: right;
}

.game-explanation {
  margin-top: 50px;
}

@include smaller($mobile-threshold) {
  // Redefine variables for smaller screens
  $field-width: 280px;
  $grid-spacing: 10px;
  $grid-row-cells: 4;
  $tile-size: ($field-width - $grid-spacing * ($grid-row-cells + 1)) / $grid-row-cells;
  $tile-border-radius: 3px;
  $game-container-margin-top: 17px;

  html, body {
    font-size: 15px;
  }

  body {
    margin: 20px 0;
    padding: 0 20px;
  }

  h1.title {
    font-size: 27px;
    margin-top: 15px;
  }

  .container {
    width: $field-width;
    margin: 0 auto;
  }

  .score-container, .best-container {
    margin-top: 0;
    padding: 15px 10px;
    min-width: 40px;
  }

  .heading {
    margin-bottom: 10px;
  }

  // Show intro and restart button side by side
  .game-intro {
    width: 55%;
    display: block;
    box-sizing: border-box;
    line-height: 1.65;
  }

  .restart-button {
    width: 42%;
    padding: 0;
    display: block;
    box-sizing: border-box;
    margin-top: 2px;
  }

  // Render the game field at the right width
  @include game-field;

  // Rest of the font-size adjustments in the tile class
  .tile .tile-inner {
    font-size: 35px;
  }

  .game-message {
    p {
      font-size: 30px !important;
      height: 30px !important;
      line-height: 30px !important;
      margin-top: 90px !important;
    }

    .lower {
      margin-top: 30px !important;
    }
  }
}


    margin-top: 30px !important; } }

  <script src="js/classlist_polyfill.js"></script>
  <script src="js/animframe_polyfill.js"></script>
  <script src="js/keyboard_input_manager.js"></script>
  <script src="js/html_actuator.js"></script>
  <script src="js/grid.js"></script>
  <script src="js/tile.js"></script>
  <script src="js/local_storage_manager.js"></script>
  <script src="js/game_manager.js"></script>
  <script src="js/application.js"></script>
</body>
</html>
