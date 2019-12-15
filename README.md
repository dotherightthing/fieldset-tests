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
1 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
2 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
3 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
4 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
5 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
6 | `{legend}` <br> `{label}` <br> *edit* <br> `{label}` <br> `placeholder` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{label}` <br> `placeholder` | `{label}` <br> *edit text* <br> `{label}` <br> `placeholder` | `{label}` <br> `{label}` <br> `placeholder` <br> *text field* | `{label}` <br> *edit* <br> `{label}` <br> `placeholder`
7 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
8 | `{childLegend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{parentLegend}` <br>  *grouping* <br> `{childLegend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{parentLegend}` <br> *group* <br> `{then}` <br> `{childLegend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{childLegend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
9 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
10 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
11 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
12 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{label}` <br> *edit* <br> `{placeholder}` <br>
13 | `{legend}` <br> `{label}` <br> *edit* <br> `{placeholder}` | `{mainLandmark}` <br> `{legend}` <br>  *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{then}` <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{label}` <br> `{placeholder}` <br> *text field* <br> *end* <br> `{legend}` <br> *end* <br> `{mainLandmark}` | `{label}` <br> *edit* <br> `{placeholder}` <br>
14 | `{groupLabel}` `{label}` <br> *edit* <br> `{placeholder}` | `{legend}` <br>  *grouping* <br> `{groupLabel}` *grouping* <br> `{label}` <br> *edit, has auto complete* <br> `{placeholder}` | `{legend}` <br> *group* <br> `{label}` <br> *edit text* <br> `{placeholder}` | `{legend}` <br> `{label}` <br> `{placeholder}` <br> *text field* | `{groupLabel}` <br> `{label}` <br> *edit* <br> `{placeholder}` <br>
15 | `{radioGroupLabel}` <br> `{radio1Label}` <br> *radio button, not checked* <br> `{radioGroupLabel}` <br> `{radio2Label}` <br> *radio button, not checked* <br> | `{legend}` *grouping* <br> `{radioGroupLabel}` *grouping* <br> `{radio1Label}` <br> *radio button, not checked* <br> `{radio2Label}` <br> *radio button, not checked* | `{legend}` <br> *group* <br> `{radio1Label}` <br> *selected, radio button, 1 of 2* <br> `{radio2Label}` <br> *selected, radio button, 3 of 2* | `{legend}` <br> `{radio1Label}` <br> *radio button, unchecked, 1 of 2* <br> `{radio2Label}` <br> *radio button, unchecked, 2 of 2* | `{radioGroupLabel}` <br> `{radio1Label}` <br> *radio button, non-selected, 1 of 2* <br> `{radio2Label}` <br> *radio button, non-selected, 2 of 2*
