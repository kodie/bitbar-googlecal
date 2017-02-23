# BitBar Google Calendar Plugin [![Build Status](https://travis-ci.org/kodie/bitbar-googlecal.svg?branch=master)](https://travis-ci.org/kodie/bitbar-googlecal)
A plugin for [BitBar](https://github.com/matryer/bitbar) that shows your upcoming [Google Calendar](https://calendar.google.com) events.

![](/screenshot.png?raw=true)

## Requirements
* [Node.js](https://nodejs.org)
* [npm](https://npmjs.com)

## Installation

### via [BitBar CLI](https://github.com/kodie/bitbar-cli)
1. `bitbar install Productivity/googlecal.30m.js`

### Manually
1. Install Xbox Feed Plugin: ```bitbar://openPlugin?title=Google%20Calendar&src=https://raw.githubusercontent.com/kodie/bitbar-googlecal/master/googlecal.30m.js```
2. `cd` into your BitBar Plugins directory and run the following command: `npm i fs home-config googleapis google-auth-library http moment open`

## Settings
These are some settings that you can change by setting them in your `~/.bitbarrc` file:

* `clientId` - The Google API Client ID
  * Default: (The BitBar Google Calendar Client ID)
  * If you'd like to (or need to), you can get your own here: https://console.developers.google.com/start/api?id=calendar

* `clientSecret` - The Google API Client Secret
  * Default: (The BitBar Google Calendar Client Secret)
  * See notes for `clientId`

* `clientRedirect` - The redirect URL defined when setting up the Google API app
  * Default: `http://localhost:3000`
  * You will probably want to leave this alone. Currently the way it is set up is the user will be redirected to a page where the plugin will be able to capture the autorization code provided by Google.

* `calendarId` - The ID of the calendar you would like to display events from
  * Default: `primary`

* `dateFormat` - The format that dates are displayed in
  * Default: `dddd M/D`
  * For more information on date formatting, see: https://momentjs.com/docs/#/displaying/format/

* `days` - The number of days (including today) to display events for
  * Default: `7`
  * Can be set to `false` to display events up to `limit` regardless of the day

* `expandEvents` - Whether to show events that span multiple days on each day
  * Default: `true`

* `limit` - The max number of events to display
  * Default: `25`
  * If `days` is set to `false`, `limit` decides how many events are displayed

* `showAllOfToday` - Whether to show all of today's events, regardless if they happened earlier today
  * Default: `true`

* `showEmptyDays` - Whether to show days that don't have any events
  * Default: `false`
  * This currently only works if `days` is NOT set to `false`

* `serverPort` - The port to use for the listening server when authorizing the Google account
  * Default: `3000`
  * Should match the port used in `clientRedirect` URL

* `timeFormat` - The format that times are display in
  * Default: `h:mma`
  * For more information on time formatting, see: https://momentjs.com/docs/#/displaying/format/

* `tokenFile` - The file where token credentials are stored
  * Default: `.googlecal.json`

### Example
```
[googlecal]
dateFormat=ddd MM/DD/YYYY
days=false
showAllOfToday=false
```

## License
MIT. See the License file for more info.
