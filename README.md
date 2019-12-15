# `fieldset` Tests

## Usage

Start browsersync server:

```
npm run serve
```

* http://localhost:3000/
* http://192.168.1.180:3000/

---

## Screen Reader Instructions

### macOS VoiceOver

```
  Start
    Command + F5
  TestA
    List form elements using Rotor to access 'Forms Control Menu'
      [Control + Option] + U + ← →
  TestB
    Focus next form element
      [Control + Option] + Command + J
```

### iOS VoiceOver

```
  Start
    Triple-click home button
    Tap "VoiceOver"
  TestA
    Twist rotor to pick ‘Form controls’
    Swipe up and down to navigate through form elements 
```

### Windows 7 IE11 JAWS

```
  Start
    Double-click JAWS icon
  TestA
    Form elements list
      [INS] + F5
    Focus next form element
      f
```

### Windows 7 Firefox NVDA

```
  Start
    Control + Alt + N
  Quit
    [INS] + q + TAB to OK + ENTER
  TestA
    Focus next form element
      f
```

### Windows 7 IE11 NVDA

```
  Start
    Control + Alt + N
  Quit
    [INS] + q + TAB to OK + ENTER
  TestA
    Focus next form element
      f
```

### Windows 10 Home Edge Narrator

```
  `Windows logo key + Ctrl + N`
    Change what you hear when reading and interacting
      Check the option `Hear advanced detail, like help text, on buttons and other controls`
```

```
  Start
    Ctrl + Windows Key + Enter
  TestA
    [CapsLk] + Ctrl + PgUp / PdDown + Form fields
    [CapsLk] + Left Arrow / Right Arrow
```

### Android 6.0.1 Chrome Talkback

```
  Start
    Quickly press physical home button 3 times
  TestA
    Swipe up/down to change active Local Context Menu option. Forms are known as ‘controls’. 
    Swipe left and right to navigate through the page form elements 
```
---

## Test Results

### Test criteria

* `fieldset legend` is announced
* `input label` is announced
* `input` is announced
* `input placeholder` is announced
* `[role="*group*"]` is announced
* `[role="*group*"] aria-labelledby` is announced

### Test key

1. `fieldset`
2. `div > fieldset`
3. `div.display-contents > fieldset`
4. `div.grid-row > div.grid-col > fieldset`
5. `fieldset.grid-row`
6. `fieldset.display-contents`
7. `div.grid-row > div.grid-col > div.display-contents > fieldset.grid-row`
8. `fieldset > fieldset`
9. `fieldset > legend.visually-hidden`
10. `fieldset > legend.visually-hidden.display-table`
11. `fieldset.flex-row > legend.visually-hidden.display-table`
12. `form > fieldset > legend.visually-hidden.display-table`
13. `article[role="main"] > form > fieldset > legend.visually-hidden.display-table`
14. `form > fieldset > [role="group"][aria-labelledby]`
15. `form > fieldset > [role="radiogroup"][aria-labelledby]`

### Audio responses

Test| Win 7 IE11 JAWS | Win 7 FF NVDA | macOS VoiceOver | iOS VoiceOver | Win 10 Edge Narrator
---| ---| ---| ---| ---| ---
1 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
2 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
3 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
4 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
5 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
6 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputLabelText}` <br> `placeholder` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputLabelText}` <br> `placeholder` | `{inputLabelText}` <br> *edit text* <br> `{inputLabelText}` <br> `placeholder` | `{inputLabelText}` <br> `{inputLabelText}` <br> `placeholder` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputLabelText}` <br> `placeholder`
7 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
8 | `{childLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{parentLegendText}` <br>  *grouping* <br> `{childLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{parentLegendText}` <br> *group* <br> `{then}` <br> `{childLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{childLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
9 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
10 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
11 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
12 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
13 | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{mainLandmark}` <br> `{fieldsetLegendText}` <br>  *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{then}` <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* <br> *end* <br> `{fieldsetLegendText}` <br> *end* <br> `{mainLandmark}` | `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
14 | `{groupLabelText}` `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br>  *grouping* <br> `{groupLabelText}` *grouping* <br> `{inputLabelText}` <br> *edit, has auto complete* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> *group* <br> `{inputLabelText}` <br> *edit text* <br> `{inputPlaceholder}` | `{fieldsetLegendText}` <br> `{inputLabelText}` <br> `{inputPlaceholder}` <br> *text field* | `{groupLabelText}` <br> `{inputLabelText}` <br> *edit* <br> `{inputPlaceholder}` <br>
15 | `{radioGroupLabelText}` <br> `{radio1LabelText}` <br> *radio button, not checked* <br> `{radioGroupLabelText}` <br> `{radio2LabelText}` <br> *radio button, not checked* <br> | `{fieldsetLegendText}` *grouping* <br> `{radioGroupLabelText}` *grouping* <br> `{radio1LabelText}` <br> *radio button, not checked* <br> `{radio2LabelText}` <br> *radio button, not checked* | `{fieldsetLegendText}` <br> *group* <br> `{radio1LabelText}` <br> *selected, radio button, 1 of 2* <br> `{radio2LabelText}` <br> *selected, radio button, 3 of 2* | `{fieldsetLegendText}` <br> `{radio1LabelText}` <br> *radio button, unchecked, 1 of 2* <br> `{radio2LabelText}` <br> *radio button, unchecked, 2 of 2* | `{radioGroupLabelText}` <br> `{radio1LabelText}` <br> *radio button, non-selected, 1 of 2* <br> `{radio2LabelText}` <br> *radio button, non-selected, 2 of 2*
