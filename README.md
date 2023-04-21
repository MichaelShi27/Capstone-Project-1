# Capstone-Project-1: Grailz

Grailz is an e-commerce website focused on designer fashion and streetwear and curated through a singular vision.


## Screenshots

Home page:
![Home](https://i.imgur.com/Kz5jLLN.png)

Products:
![Products](https://i.imgur.com/pWuW091.png)

Checkout:
![Checkout](https://i.imgur.com/cqKjpSk.png)

Login:
![Login](https://i.imgur.com/AeoFElZ.png)

Registration:
![Registration](https://i.imgur.com/7v64bch.png)

## Snippet
One interesting bit of CSS I used was to style an infinitely scrolling image slider/banner for the home page. In addition to looping seamlessly, it also pauses when the user hovers their cursor over it. Here is the relevant code:

```
@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(calc( var(--total-width) * -1 ));
  }
}

.slider .slide-track {
  animation: scroll 25s linear infinite;
  display: flex;
  width: calc( var(--total-width) * 2 );
}

.slider .slide-track:hover {
  -webkit-animation-play-state: paused;
  -moz-animation-play-state: paused;
  -o-animation-play-state: paused;
  animation-play-state: paused;
  cursor: pointer;
}
```