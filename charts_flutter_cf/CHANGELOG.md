# Changelog

All notable changes to this project are documented by extracting
information from git commits.  This project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.10.3+cf](https://github.com/exafree/charts_cf/compare/0.10.2...0.10.3+cf) - 2020-06-10

### Direct Commits

- Release 0.10.3+cf [`519f870`](https://github.com/exafree/charts_cf/commit/519f8709cb1bf3e290c0d5017b63587b1a14d139)

### Merged Commits

- Add custom template for use by auto-changelog [`#30`](https://github.com/exafree/charts_cf/pull/30)
- Improve release process and add documentation [`#27`](https://github.com/exafree/charts_cf/pull/27)
- Add gen-changelog to Makefile [`#24`](https://github.com/exafree/charts_cf/pull/24)
- Update README.md [`#20`](https://github.com/exafree/charts_cf/pull/20)
- Fix CHANGELOGs I messed them up in the forking process [`#19`](https://github.com/exafree/charts_cf/pull/19)
- Add flutter_export_environment.sh to .gitignore [`#11`](https://github.com/exafree/charts_cf/pull/11)
- Fix issues in getMinPixels and getMaxPixels [`#10`](https://github.com/exafree/charts_cf/pull/10)

### Issues Fixed

- [`#28`](https://github.com/exafree/charts_cf/issues/28): Add custom template for use by auto-changelog [`#30`](https://github.com/exafree/charts_cf/pull/30)
- [`#23`](https://github.com/exafree/charts_cf/issues/23): Add gen-changelog to Makefile [`#24`](https://github.com/exafree/charts_cf/pull/24)
- [`#16`](https://github.com/exafree/charts_cf/issues/16): Update README.md [`#20`](https://github.com/exafree/charts_cf/pull/20)
- [`#18`](https://github.com/exafree/charts_cf/issues/18): Fix CHANGELOGs I messed them up in the forking process [`#19`](https://github.com/exafree/charts_cf/pull/19)
- [`#8`](https://github.com/exafree/charts_cf/issues/8): Fix issues in getMinPixels and getMaxPixels [`#10`](https://github.com/exafree/charts_cf/pull/10)

## 0.10.2 - 2020-05-24

### Direct Commits

- Fork google/charts and create new packages [`e221a23`](https://github.com/exafree/charts_cf/commit/e221a234916508431db96aeea16114b9a5866ba2)
* Try again, forgot to add homepage to sed script for pubspec.
* Tweak link in charts_flutter_cf/README.md to github.com/exafree/charts_cf

## 0.10.1
* Second attempt at a Fork of google/charts with pachages renamed
  from charts_common and charts_flutter to charts_common_cf and
harts_flutter_cf. Where "cf" is an acronym for "community fork".

* Fix the incorrect homepage links in the pubspec.yaml
* In Makefile fixed a typo, leaving off the _cf in `cd charts_common_cf`
  in the publish_common target. And remove a debug `ls` in test_flutter target.

## 0.10.0
* Fork of google/charts with pachages renamed from charts_common
  and charts_flutter to charts_common_cf and charts_flutter_cf.
  Where "cf" is an acronym for "community fork".

## 0.9.0
* Internal bug fixes
* Bump versions in Gemlock file due to security alerts

## 0.8.1
* Update intl version.

## 0.8.0
* Bug fixes from open source.

## 0.7.0
* Added vertical bar label

## 0.6.0
* Bars can now be rendered on line charts.
* Negative measure values will now be rendered on bar charts as a separate stack from the positive
values.
* Added a Datum Legend, which displays one entry per value in the first series on the chart. This is
 useful for pie and scatter plot charts.
* The AxisPosition enum in RTLSpec was refactored to AxisDirection to better reflect its effect on
swapping the positions of all start and end components, and not just positioning the measure axes.
* Added custom colors for line renderer area skirts and confidence intervals. A new "areaColorFn"
has been added to Series, and corresponding data to the datum. We could not use the fillColorFn for
these elements, because that color is already applied to the internal section of points on line
charts (including highlighter behaviors).

## 0.5.0
* SelectionModelConfig's listener parameter has been renamed to "changeListener". This is a breaking
change. Please rename any existing uses of the "listener" parameter to "changeListener". This was
named in order to add an additional listener "updateListener" that listens to any update requests,
regardless if the selection model has changed.
* CartesianChart's method getMeasureAxis(String axisId) has been changed to
getMeasureAxis({String axisId) so that getting the primary measure axis will not need passing any id
that does not match the secondary measure axis id. This affects users implementing custom behaviors
using the existing method.

## 0.4.0
* Fixed export file to export ChartsBehavior in the Flutter library instead of the one that resides
in charts_common. The charts_common behavior should not be used except internally in the
charts_flutter library. This is a breaking change if you are using charts_common behavior.
* Declare compatibility with Dart 2.
* BasicNumericTickFormatterSpec now takes in a callback instead of NumberFormat as the default
constructor. Use named constructor withNumberFormat instead. This is a breaking change.
* BarRendererConfig is no longer default of type String, please change current usage to
BarRendererConfig<String>. This is a breaking change.
* BarTargetLineRendererConfig is no longer default of type String, please change current usage to
BarTargetLineRendererConfig<String>. This is a breaking change.

## 0.3.0
* Simplified API by removing the requirement for specifying the datum type when creating a chart.
For example, previously to construct a bar chart the syntax was 'new BarChart<MyDatumType>()'.
The syntax is now cleaned up to be 'new BarChart()'. Please refer to the
[online gallery](https://google.github.io/charts/flutter/gallery.html) for the correct syntax.
* Added scatter plot charts
* Added tap to hide for legends
* Added support for rendering area skirts to line charts
* Added support for configurable fill colors to bar charts

## 0.2.0

* Update color palette. Please use MaterialPalette instead of QuantumPalette.
* Dart2 fixes

## 0.1.0

Initial release.
