# An Introduction to Chrome's DevTools
![A picture of the DevTools bar](https://developer.chrome.com/devtools/images/devtools-window.png)
>*"The Chrome Developer Tools (DevTools for short), are a set of web authoring and debugging tools built into Google Chrome."*
>-[Chrome](https://developer.chrome.com/devtools)

Let's be honest about one thing, if DevTools wouldn't exist, it would make our developers life's much more complicated. We can use it to access the console (such a powerful tool to debug), the html file (more debugging),css (guess what, more debugging) and to use it to change lines of code and seeing it live changing without changing it first in our local file and refreshing it again. They also added a button 'Toggle device toolbar' to view the page in several iPhone's and iPads. These are the features every developer uses DevTools for.

But there is more to it than just the features mentioned above. And if you're a young developer that has a lot to learn, I suggest reading this article and getting to know DevTools better because it will save you time.

## Sources Tab
### Adding/Changing code
In the source tab you can write code just as you would do in your editor (Codeschool, no date).

When you make changes to the code in the Elements tab, these changes will disappear when you refresh the page. In the source tab you can export your changes and save them. Just like your editor it will show a star after the filename when you've made changes in the file. Changes will be saved in browser storage (Codeschool, no date).

If you do want to apply the changes to your original file you could right click inside the browser editor and click 'Save As'.

When you select 'Local Modifications' you will see the timestamps of your changes and what was changed.

### Debug Javascript
DevTools can also be used to debug JavaScript. In the tab on the far right there is a pause button. When you click pause and reload the script it will pause the code on the spot where an error occurs and will show it to you. If a variable isn't set correctly DevTools will show you the value of the variable (Codeschool, no date).

#### More readable code
As a developer you could minify your code to make performance better of your webpage but it does make your script a lot harder to read.

If your code is minified, you could click the curly brackets at the bottom of the screen to 'unminify' and debug it if necessary (Codeschool, no date).

#### Breakpoints
By adding a breakpoint to your script, you could pause your script when it comes across a breakpoint and discover when an event occurs. The highlighted line will not be executed.

In the editor you could create a breakpoint by clicking on the number of the line you want to pause. After adding a breakpoint, on the right top side of DevTools you can click the resume button to resume executing your script. Next to the resume button there is a 'Step Over' button, this will execute the next line of code. Next to that there is the 'Step into' button, which will execute whatever is inside the function of the highlighted line of code. Up next, 'Step out of' button will step out of the function and return to its collar. The last button will remove all of the breakpoints (Codeschool, no date).

## Network Tab
In the network tab, DevTools will give you insights on how long your page takes to load and which files loads in what order. The network panel is very handy for testing how your page is loaded on different network speeds.

To use it click on the tab and refresh the browser to see it in action.

### Emulating user experience
A Developers device always has faster internet than your typical user. To test that Chrome added a dropdown with several network throttling. After selecting one, you can refresh the page and see how your page does with slower internet connection (Developer Chrome, May 12, 2017). Also check the 'Disable cache' button to prevent the browser from using cached files.

After refreshing the page a table inside DevTools is rendered with all the needed files for the page. In the table you can see name, method (GET or POST), status (200:downloaded, 304:cached file etc.), type of file, initiator (executed by), size, time of load and a specific timeline. Hovering on files in the timeline will give you an explanation about the colors used and more (LevelUpTuts, October 12, 2015).

#### Filter button
On default the filter bar will be displayed. If not you can click the funnel on the top left side to toggle the filter. In the filter bar you can filter on file types (LevelUpTuts, October 12, 2015).

## Performance/Timeline Tab
The Performance or Timeline tab (depending on your version of Chrome) focusses more on (you would never guess) performance. It will show you some screenshots of the page during loading. With the screenshots you can see the order of elements that are being rendered (Fog City Learning, April 15, 2017).

It also shows you some information about JavaScript memory usage, number of documents shown, the number of nodes etc. (Fog City Learning, April 15, 2017).

## And so much more
So far we have talked about the basics but there is so much more to discover inside DevTools such as clearing storage and caching but also viewing service worker but that's a topic I will be discussing next time.

## Sources
1. Developer Chrome. (no date). *Chrome DevTools Overview*. Source:
https://developer.chrome.com/devtools
2. Codeschool. (no date). *DevTools*. Source:
http://discover-devtools.codeschool.com/
3. Developer Chrome. (May 12, 2017). *Get started with Analyzing Network Performance in Chrome DevTools*. Source:
https://developers.google.com/web/tools/chrome-devtools/network-performance/
4. LevelUpTuts. (October 12, 2015). *Website Performance Tutorial #4 - Chrome Dev Tools Network Tab Explained*. Source:
https://www.youtube.com/watch?v=yWQlra6hlwk
5. Fog City Learning. (April 15, 2017). *Chrome DevTools Tutorial 11: Performance / Timeline, Memory, Security*. Source:
https://www.youtube.com/watch?v=oWeC_bj8sI4
