### Directory Structure

```
app/
    manifests/       Where manifests are held, see Android Manifest
    java/
        android/
        test/
        src/         Where code is stored
    res/             Resources
        drawable/    All things that are drawn, e.g. pictures & icons
        layout/      Layouts of different screens
        mipmap/      Different sizes of images
        values/      Reusable values, e.g. colors or text (think languages)
```

### Android Manifest

A high-level overview of the requirements to build & run the application. For example, it defines recommended hardware levels, permissions, and specifies the entry point \(because Java doesn't have a definitive \`main\` method\).

### Activity

An activity is a single 'focus point' of a user's interaction with the application. Extends `Activity` class and requires implementation of the `onCreate` method.

An application will normally have a number of activities which the user moves between. A stack of activities is maintained, so when you complete the topmost one, you are returned to the activity you left from.

Use _intents _to start/move to other activities.

`onCreate` typically does:

* Calls the superclass
* Recovers any state information
* Set's the UI layout
* Obtains references to widgets and sets up event listeners

### View

A **View** is a basic 'building block' of a GUI. It has an `onDraw` method that is called when it is placed on the screen. All basic widgets extend this class, e.g. `Button`, `CheckBox`, `TextView`. If you want to create a custom widget, you must override the `onDraw` method.

### ViewGroup

A **ViewGroup **\(also a View\) allows you to aggregate multiple widgets into larger one. Layout components, like `ConstraintLayout` or `LinearLayout` extent the `ViewGroup` class.

### Describes the application

* Points to the Main Activity for the application.
* Holds Application Components
* Intent Filters
* Permissions
* Icons, Labels, etc
* Required hardware & software features

**Main Activity class**

* Has an `onCreate` method, executed when program starts.
  * The app's entry point.
  * Sets the content view based on the layout in resources.
* 


