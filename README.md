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
2. `fieldset` in `div`
3. `fieldset` in `div` with `display:contents`
4. `fieldset` in grid `div`s
5. `fieldset` as grid row
6. `fieldset` as `display:contents`
7. `fieldset` as nested grid row inside `display:contents`
8. Nested `fieldset`
9. `fieldset` with visually hidden `legend`
10. `fieldset` with visually hidden `legend` with `display:table`
11. `fieldset` as flex row, with visually hidden `legend` with `display:table`
12. `fieldset` within form, with visually hidden `legend` with `display:table`
13. `fieldset` within form within `article[role="main"]`, with visually hidden `legend` with `display:table`
14. `[role="*group*"]` with `[aria-labelledby]` within `fieldset` within `form`

### Audio responses

Test| Win 7 IE11 JAWS | Win 7 FF NVDA | macOS VoiceOver | iOS VoiceOver | Win 10 Edge Narrator
---|---|---|---|---|---
1 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
2 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
3 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
4 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
5 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
6 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputLabelText}`<br> `placeholder` | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputLabelText}`<br> `placeholder` | `{inputLabelText}`<br>*edit text*<br>`{inputLabelText}`<br> `placeholder` | `{inputLabelText}`<br>`{inputLabelText}`<br> `placeholder`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputLabelText}`<br> `placeholder`
7 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
8 | `{childLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{parentLegendText}`<br>  *grouping*<br> `{childLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{parentLegendText}`<br>*group*<br>`{then}`<br>`{childLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{childLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
9 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
10 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
11 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
12 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field* | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
13 | `{fieldsetLegendText}`<br> `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{mainLandmark}`<br>`{fieldsetLegendText}`<br>  *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{then}`<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{inputLabelText}`<br>`{inputPlaceholder}`<br>*text field*<br>End`{fieldsetLegendText}`<br>, End`{mainLandmark}`<br> | `{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
14 |`{ariaLabelledByText}` `{inputLabelText}`<br> *edit*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>  *grouping*<br>`{ariaLabelledByText}` *grouping*<br> `{inputLabelText}`<br> *edit, has auto complete*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>*group*<br>`{inputLabelText}`<br>*edit text*<br>`{inputPlaceholder}`<br> | `{fieldsetLegendText}`<br>`{inputLabelText}`<br>`{inputPlaceholder}`<br> *text field* |`{ariaLabelledByText}`<br>`{inputLabelText}`<br>*edit*<br>`{inputPlaceholder}`<br>
