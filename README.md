# AndroidDateTimePicker

[![Min SDK](https://img.shields.io/badge/Min%20SDK-5.0-green.svg?style=flat-square)](https://developer.android.com/studio/releases/platforms#5.0)
[![Lincense](https://img.shields.io/badge/Lincense-Apache%202.0%20License-orange.svg?style=flat-square)](https://github.com/Fei-Sheng-Wu/AndroidDateTimePicker/blob/1.0.0/LICENSE.txt)

> An date and/or time picker for Android. Light theme design, full screen picker dialog and native Material components. Support setting default selected date time and result submit callback handling listener. Support custom button icon, title text and theme color. Min SDK is SDK 5.0 and support AndroidX.

## Dependencies

**Min SDK** = 5.0

## Main Features

- [x] Date and time picker
- [x] Date picker
- [x] Default selected date time setting
- [x] Result callback listener
- [x] Custom button icons
- [x] Custom title text
- [x] Custom theme color

## Screenshot

<figure class="video_container">
  <video controls="true" allowfullscreen="true" poster="path/to/poster_image.png">
    <source src="https://github.com/Fei-Sheng-Wu/AndroidDateTimePicker/blob/1.0.0/Screenshot/DateTimePicker.mp4" type="video/mp4">
  </video>
</figure>

![DateTimePicker Select Date](https://github.com/Fei-Sheng-Wu/AndroidDateTimePicker/blob/1.0.0/Screenshot/DateTimePicker%20Select%20Date.png)
![DateTimePicker Select Time](https://github.com/Fei-Sheng-Wu/AndroidDateTimePicker/blob/1.0.0/Screenshot/DateTimePicker%20Select%20Time.png)

## How to Use

It is very simple to use.

```java
DateTimePickerDialog selectDialog = new DateTimePickerDialog();
selectDialog.setDefaultDateTime(Calendar.getInstance()); //Set default selected date time.
selectDialog.setOnResultsListener(new DateTimePickerDialog.OnResultsListener() {
    @Override
    public void onSuccess(Calendar date) {
        //On result submited callback listener.
    }
});
getSupportFragmentManager().beginTransaction()
    .setTransition(FragmentTransaction.TRANSIT_FRAGMENT_OPEN) //Set the transition animation when dialog opened.
    .add(R.id.root_view, selectDialog) //Show dialog. "R.id.root_view" should be replaced by the ID of activity's root view.
    .addToBackStack(null) //Add dialog to back stack.
    .commit();
```

Added these to string.xmls to change title text.

```xml
<string name="title_select_date">Select Date</string>
<string name="title_select_time">Select Time</string>
```

Added these to colors.xmls to change theme color.

```xml
<color name="colorPrimary">#FFFFFF</color>
<color name="colorPrimaryDark">#FFFFFF</color>
<color name="colorAccent">#000000</color>
<color name="colorControl">#EDEDED</color>
```

Added these drawable to drawable directory to change button icons.

|Drawable Name|Used For|Icon Size|
|--------   |--------   |--------   |
|ic_close_24.xml|Close picker dialog for canceling selection button. |24dp x 24dp|
|ic_next_24.xml|Switch from date selection to time selection button.|24dp x 24dp|
|ic_submit_24.xml|Submit selected result button.|24dp x 24dp|

## License

This project is under the [Apache 2.0 License](https://github.com/Fei-Sheng-Wu/AndroidDateTimePicker/blob/1.0.0/LICENSE.txt).
