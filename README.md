# Google Developer Group Finder
- App to discover GDG's in your area.
- Made with Google Code Labs!
- Material Design

#### Summary
- Use themes, styles, and attributes on views to change the appearance of views.
Themes affect the styling of your whole app and come with many preset values for colors, fonts, and font sizes.
An attribute applies to the view in which the attribute is set. Use attributes if you have styling that applies to only one view, such as padding, margins, and constraints.
Styles are groups of attributes that can be used by multiple views. For example, you can have a style for all your content headers, buttons, or text views.
Themes and styles inherit from their parent theme or style. You can create a hierarchy of styles.
Attribute values (which are set in views) override styles. Styles override the default style. Styles override themes. Themes override any styling set by the textAppearance property.
- Using downloadable fonts makes fonts available to users without increasing the size of your APK. To add a downloadable font for a view:

Select the view in the Design tab, and select More fonts from the drop-down menu of the fontFamily attribute.
In the Resources dialog, find a font and select the Create downloadable font radio button.
Verify that the Android manifest includes a meta-data tag for preloaded fonts.
When the app first requests a font, and the font is not already available, the font provider downloads it from the internet