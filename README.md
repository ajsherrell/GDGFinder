# Google Developer Group Finder
- App to discover GDG's in your area.
- Made with Google Code Labs!
- Material Design
- Accessibility
- RTL
- Chips
- Night Mode

### Material Design
- Material Design is a cross-platform design system from Google, and is the design system for Android. Material Design provides detailed specs for everything in an app's user interface (UI), from how text should be shown, to how to lay out a screen. The Material Design website at material.io has the complete specifications.

On material.io you can also find a list of additional views that ship with Material Design components. The views include bottom navigation, a floating action button (FAB) that you use in this codelab, chips that you explore in the next codelab, and collapsing toolbars.

In addition to these views that you can use to implement Material Design, the Material Design components library exports the MaterialComponents theme that your app already uses. The MaterialComponents theme implements Material Design for controls, uses theme attributes, and is customizable.

### Accessibility
- To make an app usable by the most users makes sense, whether you are developing for the joy of it, or for business purposes. There are multiple dimensions to accomplishing that.

Support RTL Languages. European and many other languages read from left to right, and apps originating from those locales are commonly designed to fit well for those languages. Many other languages with a large number of speakers read from right to left, such as Arabic. Make your app work with right-to-left (RTL) languages to increase your potential audience.
Scan for accessibility. Guessing at how someone else may experience your app is an option with pitfalls. The Accessibility Scanner app takes the guess work out of the loop and analyses your app, identifying where you could improve its accessibility.
Design for TalkBack with content descriptions. Visual impairments are more common than one might think, and many users, not just blind ones, use a screen reader. Content descriptions are phrases for a screen reader to say when a user interacts with an element of the screen.
Support night mode. For many visually impaired users, changing the screen colors improves contrast and helps them visually work with your app. Android makes it straightforward to support night mode, and you should always support night mode to give users a simple alternative to the default screen colors. You can use chips to make your app more interesting, while keeping it accessible.

### Chips
- Chips are compact elements that represent an attribute, text, entity, or action. They allow users to enter information, select a choice, filter content, or trigger an action.
- To create a group of chips, use a com.google.android.material.chip.ChipGroup.
Define the layout for one com.google.android.material.chip.Chip.
If you want your chips to change colors, provide a color state list as a <selector> with stateful colors:
<item android:color="?attr/colorPrimaryVariant"
android:state_selected="true" />
Bind the chips to live data by adding an observer to the data in the view model.
To display the chips, create an inflator for the chip group:
LayoutInflater.from(chipGroup.context)
Create the chips, add a click listener that triggers the desired action, and add the chips to the chip group.

### Night Mode
- Use the DayNight AppTheme to support dark mode.
You can set dark mode programmatically:
AppCompatDelegate.setDefaultNightMode()
Create a res/values-night resource folder to provide custom colors and values for dark mode.

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
