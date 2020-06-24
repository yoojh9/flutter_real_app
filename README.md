# flutter_real_app

A new Flutter project.

## 1. Containers vs Column / Row

- Container

  - takes exactly one child widget
  - Rich alignment & Styling options
  - Flexible width (e.g child width, available width..)
  - Perfect for custom styling & alignment

- Column / Row
  - takes multiple (unlimited) child widget
  - Alignment but no styling options
  - Always takes full available height(column) / width(row)
  - Must-use if widgets sit next to / above each other

## 2. dart dateformat

- https://pub.dev/packages/intl : This package provides internationalization and localization facilities, including message translation, plurals and genders, date/number formatting and parsing, and bidirectional text.

- 아래 dependecy를 pubspect.yaml 파일에 붙여넣는다.

```
dependencies:
  intl: ^0.16.1
```

- The intl package supports a broad range of date formatting patterns. Here's a list

```
 DAY                          d
 ABBR_WEEKDAY                 E
 WEEKDAY                      EEEE
 ABBR_STANDALONE_MONTH        LLL
 STANDALONE_MONTH             LLLL
 NUM_MONTH                    M
 NUM_MONTH_DAY                Md
 NUM_MONTH_WEEKDAY_DAY        MEd
 ABBR_MONTH                   MMM
 ABBR_MONTH_DAY               MMMd
 ABBR_MONTH_WEEKDAY_DAY       MMMEd
 MONTH                        MMMM
 MONTH_DAY                    MMMMd
 MONTH_WEEKDAY_DAY            MMMMEEEEd
 ABBR_QUARTER                 QQQ
 QUARTER                      QQQQ
 YEAR                         y
 YEAR_NUM_MONTH               yM
 YEAR_NUM_MONTH_DAY           yMd
 YEAR_NUM_MONTH_WEEKDAY_DAY   yMEd
 YEAR_ABBR_MONTH              yMMM
 YEAR_ABBR_MONTH_DAY          yMMMd
 YEAR_ABBR_MONTH_WEEKDAY_DAY  yMMMEd
 YEAR_MONTH                   yMMMM
 YEAR_MONTH_DAY               yMMMMd
 YEAR_MONTH_WEEKDAY_DAY       yMMMMEEEEd
 YEAR_ABBR_QUARTER            yQQQ
 YEAR_QUARTER                 yQQQQ
 HOUR24                       H
 HOUR24_MINUTE                Hm
 HOUR24_MINUTE_SECOND         Hms
 HOUR                         j
 HOUR_MINUTE                  jm
 HOUR_MINUTE_SECOND           jms
 HOUR_MINUTE_GENERIC_TZ       jmv
 HOUR_MINUTE_TZ               jmz
 HOUR_GENERIC_TZ              jv
 HOUR_TZ                      jz
 MINUTE                       m
 MINUTE_SECOND                ms
 SECOND                       s
```

Examples Using the US Locale:

```
 Pattern                           Result
 ----------------                  -------
 new DateFormat.yMd()             -> 7/10/1996
 new DateFormat("yMd")            -> 7/10/1996
 new DateFormat.yMMMMd("en_US")   -> July 10, 1996
 new DateFormat.jm()              -> 5:08 PM
 new DateFormat.yMd().add_jm()    -> 7/10/1996 5:08 PM
 new DateFormat.Hm()              -> 17:08 // force 24 hour time
```

## 3. ListView

- Column -> ListView
- A ListView is scrollable by default
- ListView is the most commonly used scrolling widget
- ListView(children:[])
  - wrapping SingleChildScrollView()
- ListView.builder()
  - only load what's visible
  - 아이템 갯수가 많을 때는 ListView.builder()를 고려해라.

## 4. Useful Resources & Links

- More on Layouting (with Column(), Row() etc). : [https://flutter.dev/docs/development/ui/layout](https://flutter.dev/docs/development/ui/layout)
- More on Images & Assets: [https://flutter.dev/docs/development/ui/assets-and-images](https://flutter.dev/docs/development/ui/assets-and-images)
- Official Widget Catalog: [https://flutter.dev/docs/development/ui/widgets](https://flutter.dev/docs/development/ui/widgets)
- Material Design Docs: [https://material.io/design/](https://material.io/design/)
- Flutter Theming: [https://flutter.dev/docs/cookbook/design/themes](https://flutter.dev/docs/cookbook/design/themes)

## 5. What does "Responsive" Mean?

support different device size (Portrait-mode phone, Landscape-mode phone, Tablet, Desktop PC)

## 6. What does "Adaptive" Mean?

probably diffrent look and feel on IOS and Android

- Android

  - Meterial-Design Look / Styles
  - Android Animations / Route Trainsitions
  - Android Fonts

- iOS
  - Cupertino Look / Styles
  - iOS Animations / Route Transitions
  - iOS Fonts

## 7. Responsive & Adaptive Apps in Flutter

<img src="./capture.png" width="600px">
