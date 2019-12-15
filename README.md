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
* `[role="group"]` is announced
* `[role="group"] aria-labelledby` is announced

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
14. `[role="group"]` with `[aria-labelledby]` within `fieldset` within `form`

### Audio responses

Test| Win 7 IE11 JAWS | Win 7 FF NVDA | macOS VoiceOver | iOS VoiceOver | Win 10 Edge Narrator
---|---|---|---|---|---
1 | Test1 `legend` Test1 `input` Edit Test1 `input` `placeholder` | Test1 `legend`  grouping; Test1 `input` :  edit  has auto complete  Test1 `input` `placeholder` | Test1 `legend`, group + Test1 `input`, edit text, Test1 `input` `placeholder` | Test1 `legend`, Test1 `input`, Test1 `input` `placeholder`, Text Field | Test1 `input`, Edit, Test1 `input` `placeholder`
2 | Test2 `legend` Test2 `input` Edit Test2 `input` `placeholder` | Test2 `legend`  grouping; Test2 `input` :  edit  has auto complete  Test2 `input` `placeholder` | Test2 `legend`, group + Test2 `input`, edit text, Test2 `input` `placeholder` | Test2 `legend`, Test2 `input`, Test2 `input` `placeholder`, Text field | Test2 `input`, Edit, Test2 `input` `placeholder`
3 | Test3 `legend` Test3 `input` Edit Test3 `input` `placeholder` | Test3 `legend`  grouping; Test3 `input` :  edit  has auto complete  Test3 `input` `placeholder` | Test3 `legend`, group + Test3 `input`, edit text, Test3 `input` `placeholder` | Test3 `legend`, Test3 `input`, Test3 `input` `placeholder`, Text field | Test3 `input`, edit, Test3 `input` `placeholder`
4 | Test4 `legend` Test4 `input` Edit Test4 `input` `placeholder` | Test4 `legend`  grouping; Test4 `input` :  edit  has auto complete  Test4 `input` `placeholder` | Test4 `legend`, group + Test4 `input`, edit text, Test4 `input` `placeholder` | Test4 `legend`, Test4 `input`, Test4 `input` `placeholder`, Text field | Test4 `input`, edit, Test4 `input` `placeholder`
5 | Test5 `legend` Test5 `input` Edit Test5 `input` `placeholder` | Test5 `legend`  grouping; Test5 `input` :  edit  has auto complete  Test5 `input` `placeholder` | Test5 `legend`, group + Test5 `input`, edit text, Test5 `input` `placeholder` | Test5 `legend`, Test5 `input`, Test5 `input` `placeholder`, Text field | Test5 `input`, edit, Test5 `input` `placeholder`
6 | Test6 `legend` Test6 `input` Edit Test6 `input` `placeholder` | Test6 `legend`  grouping; Test6 `input` :  edit  has auto complete  Test6 `input` `placeholder` | Test6 `input`, edit text, Test6 `input` `placeholder` | Test6 `input`, Test6 `input` `placeholder`, Text field | Test6 `input`, edit, Test6 `input` `placeholder`
7 | Test7 `legend` Test7 `input` Edit Test7 `input` `placeholder` | Test7 `legend`  grouping; Test7 `input` :  edit  has auto complete  Test7 `input` `placeholder` | Test7 `legend`, group + Test7 `input`, edit text, Test7 `input` `placeholder` | Test7 `legend`, Test7 `input`, Test7 `input` `placeholder`, Text field | Test7 `input`, edit, Test7 `input` `placeholder`
8 | Test8 child `legend` Test8 `input` Edit Test8 `input` `placeholder` | Test8 parent `legend`  grouping; Test8 child `legend`  grouping; Test8 `input` :  edit  has auto complete  Test8 `input` `placeholder` | Test8 parent `legend`, group + Test8 child `legend`, group + Test8 `input`, edit text, Test8 `input` `placeholder` | Test8 child `legend`, Test8 `input`, Test8 `input` `placeholder`, Text field | Test8 `input`, edit, Test8 `input` `placeholder`
9 | Test9 `legend` Test9 `input` Edit Test9 `input` `placeholder` | Test9 `legend`  grouping; Test9 `input` :  edit  has auto complete  Test9 `input` `placeholder` | Test9 `legend`, group + Test9 `input`, edit text, Test9 `input` `placeholder` | Text 9 `legend`, Test9 `input`, Test9 `input` `placeholder`, Text field | Test9 `input`, edit, Test9 `input` `placeholder`
10 | Test10 `legend` Test10 `input` Edit Test10 `input` `placeholder` | Test10 `legend`  grouping; Test10 `input` :  edit  has auto complete  Test10 `input` `placeholder` | Test10 `legend`, group + Test10 `input`, edit text, Test10 `input` `placeholder` | Text 10 `legend`, Test10 `input`, Test10 `input` `placeholder`, Text field | Test10 `input`, edit, Test10 `input` `placeholder`
11 | Test11 `legend` Test11 `input` Edit Test11 `input` `placeholder` | Test11 `legend`  grouping; Test11 `input` :  edit  has auto complete  Test11 `input` `placeholder` | Test11 `legend`, group + Test11 `input`, edit text, Test11 `input` `placeholder` | Text 11 `legend`, Test11 `input`, Test11 `input` `placeholder`, Text field | Test11 `input`, edit, Test11 `input` `placeholder`
12 | Test12 `legend` Test12 `input` Edit Test12 `input` `placeholder` | Test12 `legend`  grouping; Test12 `input` :  edit  has auto complete  Test12 `input` `placeholder` | Test12 `legend`, group + Test12 `input`, edit text, Test12 `input` `placeholder` | Text 12 `legend`, Test12 `input`, Test12 `input` `placeholder`, Text field | Test12 `input`, edit, Test12 `input` `placeholder`
13 | Test13 `legend` Test13 `input` Edit Test13 `input` `placeholder` | `main` landmark; Test13 `legend`  grouping; Test13 `input` :  edit  has auto complete  Test13 `input` `placeholder` | Test13 `legend`, group + Test13 `input`, edit text, Test13 `input` `placeholder` | Test13 `input`, Test13 `input` `placeholder`, Text field, End, Test13 `legend`, End, `main` | Test13 `input`, edit, Test13 `input` `placeholder`
14 | Test14 `group label` Test14 `input` Edit Test14 `input` `placeholder` | Test14 `legend`  grouping; Test14 `group label` grouping; Test14 `input` :  edit  has auto complete  Test14 `input` `placeholder` | Test14 `legend`, group; Test14 `input`, edit text. Test14 `input` `placeholder` | Test14 `legend`. Test14 `input`. Test14 `input` `placeholder`. Text field | Test14 `group label`, Test14 `input`, edit, Test14 `input` `placeholder`
