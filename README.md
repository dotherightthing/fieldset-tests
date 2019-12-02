# Fieldset Tests

## Tests

* `legend` is announced
* `label` is announced
* `input` is announced
* `input placeholder` is announced

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
  Test A
    List form elements using Rotor to access 'Forms Control Menu'
      [Control + Option] + U + ← →
  Test B
    Focus next form element
      [Control + Option] + Command + J
```

### iOS VoiceOver

```
  Start
    Triple-click home button
    Tap "VoiceOver"
  Test A
    Twist rotor to pick ‘Form controls’
    Swipe up and down to navigate through form elements 
```

### Windows 7 + IE11 + JAWS

```
  Start
    Double-click JAWS icon
  Test A
    Form elements list
      [INS] + F5
    Focus next form element
      f
```

### Windows 7 + Firefox + NVDA

```
  Start
    Control + Alt + N
  Quit
    [INS] + q > TAB to OK > ENTER
  Test A
    Focus next form element
      f
```

### Windows 7 + IE11 + NVDA

```
  Start
    Control + Alt + N
  Quit
    [INS] + q > TAB to OK > ENTER
  Test A
    Focus next form element
      f
```

### Windows 10 Home + Edge + Narrator

```
  Start
    Ctrl + Windows Key + Enter
  Test A
    [CapsLk] + PgUp / PdDown > Form fields
    [CapsLk] + Left Arrow / Right Arrow
```

### Android 6.0.1 + Chrome + Talkback

```
  Start
    Quickly press physical home button 3 times
  Test A
    Swipe up/down to change active Local Context Menu option. Forms are known as ‘controls’. 
    Swipe left and right to navigate through the page form elements 
```
---

## Test Results

### Test 1: Fieldset

```
Test A
  macOS VoiceOver
    OK
  iOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus
```

### Test 2: Fieldset in DIV

```
Test A
  macOS VoiceOver
    OK
  iOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus
```

### Test 3: Fieldset in DIV with display contents

```
Test A
  macOS VoiceOver
    OK
  iOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus
```

### Test 4: Fieldset in grid DIVs

```
Test A
  macOS VoiceOver
    OK
  iOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus
```

### Test 5: Fieldset as grid row

```
Test A
  macOS VoiceOver
    OK
  iOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus
```

### Test 6: Fieldset as display contents

```
Test A:
  macOS VoiceOver
    Legend not announced on focus
  iOS VoiceOver
    Legend not announced on focus
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus

Test B:
  macOS VoiceOver
    Legend not announced
```

### Test 7: Fieldset as nested grid row inside display contents

```
Test A:
  macOS VoiceOver
    OK
  iOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    OK
  Windows 7 + Firefox + NVDA
    OK
  Windows 7 + IE11 + NVDA
    Legend not announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
    Legend not announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
    Legend not announced on focus
```

### Test 8: Nested Fieldset

```
Test A:
  macOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    Parent legend not announced on focus
  Windows 7 + Firefox + NVDA
    OK
  iOS VoiceOver
    Parent legend not announced on focus
  Windows 7 + IE11 + NVDA
    Neither legend announced on focus
    Placeholder not announced on focus
  Windows 10 Home + Edge + Narrator
     Neither legend announced on focus
    Placeholder not announced on focus
  Android 6.0.1 + Chrome + Talkback
     Neither legend announced on focus
```

### Test 9: Fieldset with visually hidden legend

```
Test A:
  macOS VoiceOver
    TODO
  Windows 7 + IE11 + JAWS
    TODO
  Windows 7 + Firefox + NVDA
    TODO
  iOS VoiceOver
    OK
  Windows 7 + IE11 + NVDA
    TODO
  Windows 10 Home + Edge + Narrator
    TODO
  Android 6.0.1 + Chrome + Talkback
    TODO
```

### Test 10: Fieldset with visually hidden legend with display:table

```
Test A:
  macOS VoiceOver
    TODO
  Windows 7 + IE11 + JAWS
    TODO
  Windows 7 + Firefox + NVDA
    TODO
  iOS VoiceOver
    OK
  Windows 7 + IE11 + NVDA
    TODO
  Windows 10 Home + Edge + Narrator
    TODO
  Android 6.0.1 + Chrome + Talkback
    TODO
```

### Test 11: Fieldset as flex row, with visually hidden legend with display:table

```
Test A:
  macOS VoiceOver
    TODO
  Windows 7 + IE11 + JAWS
    TODO
  Windows 7 + Firefox + NVDA
    TODO
  iOS VoiceOver
    OK
  Windows 7 + IE11 + NVDA
    TODO
  Windows 10 Home + Edge + Narrator
    TODO
  Android 6.0.1 + Chrome + Talkback
    TODO
```

### Test 12: Fieldset within form, with visually hidden legend with display:table

```
Test A:
  macOS VoiceOver
    TODO
  Windows 7 + IE11 + JAWS
    TODO
  Windows 7 + Firefox + NVDA
    TODO
  iOS VoiceOver
    OK
  Windows 7 + IE11 + NVDA
    TODO
  Windows 10 Home + Edge + Narrator
    TODO
  Android 6.0.1 + Chrome + Talkback
    TODO
```

### Test 13: Fieldset within form within article, with visually hidden legend with display:table

```
Test A:
  macOS VoiceOver
    OK
  Windows 7 + IE11 + JAWS
    TODO
  Windows 7 + Firefox + NVDA
    TODO
  iOS VoiceOver
    Legend not announced
  Windows 7 + IE11 + NVDA
    TODO
  Windows 10 Home + Edge + Narrator
    TODO
  Android 6.0.1 + Chrome + Talkback
    TODO
```