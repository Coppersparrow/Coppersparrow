// Wiggle The Antenna
const wiggleAntenna = () => {
  const antenna_one = document.querySelector('#antenna-1')
  const antenna_one_ball = document.querySelector('#antenna-1-ball')
  const antenna_two = document.querySelector('#antenna-2')
  const antenna_two_ball = document.querySelector('#antenna-2-ball')

  const wiggle = new TimelineMax()
  wiggle.to(antenna_one, 0.1, {attr: {d: "M 54 5 q 10 10 0 50"}, repeat: 1, yoyo: true})
    .to(antenna_one, 0.1, {attr: {d: "M 54 5 q -10 10 0 50"}, repeat: 1, yoyo: true})

  TweenMax.to(antenna_one_ball, 0.1, {repeat: 1, yoyo: true, x:1, y:0})

  // same for the other antenna and ball
}

// Make The Robot Blink
const blink = () => {
  const eye = document.querySelector('#eye-1')
  const eye2 = document.querySelector('#eye-2')

  TweenMax.to([eye, eye2], 0.2, { scaleY: 0, yoyo: true, repeat: 1, transformOrigin: 'center'})
}

// Making The Robot Move
const moveUpAndDown = () => {
  const body = document.querySelector('#body')
  const head = document.querySelector('#head')
  const arms = document.querySelector('#arms')

  TweenMax.to([body, head, arms], 0.3, {y: '20px', yoyo: true})
}

// BOUS — Sleep and Wake
const sleep = () => {
  // close eyes
}

const wake = () => {
  // open eyes
}
