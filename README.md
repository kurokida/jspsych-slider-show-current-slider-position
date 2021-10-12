# jspsych-slider-show-current_slider_position

This is a plugin that modifies [the jspsych-html-slider-response plugin](https://www.jspsych.org/7.0/plugins/html-slider-response/) to display the current slider position as a number.

## Properties specific to this plugin

Please set the show_slider_pos property as `ture` to present the current slider position.

```javascript
show_slider_pos: {
  type: jsPsych.plugins.parameterType.BOOL,
  pretty_name: 'Show the current slider position',
  default: false,
  description: 'If true, the current slider position is presented.'
}

prompt_slider_pos1: {
  type: jsPsych.plugins.parameterType.STRING,
  pretty_name: 'Prompt immediately before the current slider position.',
  default: 'The current slider position is ',
  description: 'Any content here will be displayed immediately before the current slider position.'
}

prompt_slider_pos2: {
  type: jsPsych.plugins.parameterType.STRING,
  pretty_name: 'Prompt immediately after the current slider position.',
  default: '.',
  description: 'Any content here will be displayed immediately after the current slider position.'
}

```

## Sample code where the prompt is written in Japanese.

```javascript
  var trial_1 = {
    type: 'html-slider-response',
    stimulus: '<div style="margin: 50px auto; width: 100px; height: 100px; background-color: rgb(46, 26, 122);"></div>',
    labels: ['Purple', 'Blue'],
    slider_width: 500,
    require_movement: true,
    prompt: '<p>Is this color closer to purple or blue? Use the slider above.</p>',
    show_slider_pos: true,
    prompt_slider_pos1: '現在のスライダーの位置は',
    prompt_slider_pos2: 'です。'
  }
```
