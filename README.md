
<p align="center">
  <img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/live.png" />
</p>

<p align="center">
  <img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/LineChart.gif" />
  <img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/BarChart.gif" />
  <img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/StackedBarChart.gif" />
  <img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/PieChart.gif" />
  <img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/ScatterChart.gif" />
</p>

Live charts is an easy way to build useful charts, all charts are animated, they update every time you change your data, or when you rezise the chart, also since 0.5 we are working to support huge amounts of data, right now this is on test and only implemented in line chart, but in the included examples it is able to draw 1'000,000 points in a really short period of time.

 - MVVM Charting, Support for WPF Binding, All charts update when data changes.
 - Good looking, animated and easy to customize charts, you can practically change all properties.
 - Easy to maintain and create new charts, as you can see in the source code, some charts have almost no code.
 - Supports zooming and panning.
 - MIT License, permissive licensing.
 
This is the logic you use in every chart, there are just some litle properties or rules that change from each type of chart.

**XAML**
```xml
<liveCharts:LineChart Name="Chart">
    <liveCharts:LineChart.Series>
       <liveCharts:LineSeries Name="MariaSeries" Title="Maria" PrimaryValues="{Binding}" />
       <liveCharts:LineSeries Name="JohnSeries" Title="John" PrimaryValues="{Binding}" />
     </liveCharts:LineChart.Series>
</liveCharts:LineChart>
```
**Code Behind**

```c#
MariaSeries.DataContext = new ObservableCollection<double> {2, 3, 5, 7};
JohnSeries.DataContext = new ObservableCollection<double> {7, 3, 4, 1};
//you can add more series too!
Chart.Series.Add(new LineSeries
{
    Title = "Charles",
    PrimaryValues = new ObservableCollection<double> { 5, 8, 1, 9}
});
```

# Installation

**1**. Install package from [**Nuget**](https://www.nuget.org/packages/LiveCharts) `Install-Package LiveCharts`


**2**. Add name space to your `XAML` 
```
xmlns:liveCharts="clr-namespace:LiveCharts;assembly=LiveCharts"
```
**3**. Thats it. You are ready.

# How to Contribute

* Star this repo
* Try it
* Report Issues and Improvements
* Pull request are well received

# Need examples?

Try [Live Charts Wiki](https://github.com/beto-rodriguez/Live-Charts/wiki), or cloning this repo, test project includes a lot of examples, copy and paste this link in your browser for a cloning shortcut
```
git-client://clone?repo=https%3A%2F%2Fgithub.com%2Fbeto-rodriguez%2FLive-Charts
```

# More Images

<p align="center">
<img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/Tooltip.gif" />
</p>
<p align="center">
<img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/multiseries.png" />
</p>
<p align="center">
<img src="https://dl.dropboxusercontent.com/u/40165535/LiveCharts/UiElements.png" />
</p>
