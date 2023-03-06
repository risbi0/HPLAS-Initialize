# HPLAS-Initialize

Scripts used for initializing the data for [Hololive-Production-Livestream-Activity-Statistics](https://github.com/risbi0/Hololive-Production-Livestream-Activity-Statistics).

Data was gathered using [Holodex API](https://holodex.stoplight.io/) with the [holodex.js](https://github.com/HolodexNet/holodex.js) library.

### Setup

Install libraries:
```bash
npm install
```

### Scripts

`holodexVidIds.js` extracts all video ID's of a specific VTuber in its Holodex channel page. It is entered in the dev console where it loops with a delay to let all the links to render on each page, and extract them using the DOM API. The printed result is put in `channel_vid_ids.json`.

`holodexApiClient.js` queries the Holodex API through an array of ID's in `channel_vid_ids.json`, and extracts the interested details in the response. Data is stored in an object and then saved into a JSON file named `livestream_details.json`.