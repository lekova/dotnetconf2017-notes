# dotnetconf2017-notes
my notes on www.dotnetconf.com

### 1. Keynote [here](https://github.com/lekova/dotnetconf2017-notes/blob/master/keynote.md)

### 2. What's new in APS.NET Core 2.0
    + Install .NET Core 2.0. from https://dot.net/core
    + Install VS from https://visualstudio.com

+ Get started faster

Create nwe project with `dotnet new web -o myapp` where `-o` is for output directory. the restore is already run for us so we don't have to run it manually. Most of the packages have been consolidated in `Microsoft.AspNetCore.All` package.

The `runtime store` already includes all binaries so the app doesn't have to bring them when publishing 2.0. in and as a result the app is smaller.

Configuration is so important that is now part of ASP.NET Core. It's accessible by DI. Logging is pushed to Whe webHosst now.

+ Razor pages - 
```[TempData]``` annotation for properties. is different from Viewdata. it's intended for 

+ Authentication 

Now it's only app.UseAuthentication() combining middleware like cookies, facebook.. etc. Now with 1 middleware we can't clash and try to do them in the same time like before.

Online Authenticator App [GAuth](http://gauth.apps.gbraad.nl/)

+ Spa Templates - Angular, React React/Redux

When having Angular project we can change things, save the file and webpack monitors for changes and updates the page in the browsers.

+ Performance 

Startup performance compared to 1.1 is going down to 00:00:00.55 from 00:00:03.75 😱
  That's because the pages are precompiled, and the views. Runtime store has all binaries so we save the time to jitter.
  
+ Seamless Diagnostics

Lightup feature - w/o writing a single line of code. Starts AppInsights in Azure

### 3. Diagnostics 101

+ Exclude parts of the code until the problem's found. Exclude whole folders with files that are expected to do something related to the issue we are having.

+ Things to be sceptical of
  + *Your code* - kinda obvious
  + *The debugger's Immediate Window* - better use watches and locals
  + *The debugger's string representation* problem with back slashes in the debugger. Always shows them are \\
  + *Console output (examples: string, floating point)*
  + *Articles from a few months ago* 


## Announcements
.Net Foundation starts sport User groups. They will start Meetup Pro user groups.
![meetup groups](https://github.com/lekova/dotnetconf2017-notes/blob/master/images/meetup_progroup_announcement.png)

## Links
+ .NET Foundation meetups https://dotnetfoundation.org/events
+ Meetup Pro https://www.meetup.com/pro/dotnet/
+ dotnet Presentations https://dotnet-presentations/dotnetcore-workshop
+ questions about .NET standard https://aka/ms/netstandardfaq to Immo Landwerth
