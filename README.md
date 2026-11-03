# Picking-up photo test

A throwaway one-page web app to answer one question: is tapping on a photo of the drive accurate enough to send the dogs to the right area?

It is plain HTML and JavaScript in a single file (`index.html`). Nothing is sent anywhere; the current photo and marks are kept in the phone's browser storage until you take a new photo.

## Put it on your phone

The camera, GPS and compass only work over HTTPS, so host it on GitHub Pages:

1. Commit `index.html` and this README to the `Pickup` repo and push to GitHub.
2. On GitHub: Settings, then Pages. Under "Build and deployment" choose "Deploy from a branch", branch `main`, folder `/ (root)`, and Save.
3. After a minute, open `https://<your-github-username>.github.io/Pickup/` in Chrome on the Galaxy S26.
4. Optional: Chrome menu, then "Add to Home screen", so it opens full screen.

## Camera and view width

The camera screen has a list of your phone's cameras. If your phone lists an ultra-wide camera there, pick it to see more of the drive. The page also asks for the camera's widest zoom.

Each camera needs its view width measured once. Take a photo, put two or three marks at least 30 yds away (one well left of centre, one well right), press **I'm here** at each, then press **Fit view width** in **Results**. The value is saved for that camera. Rough starting points: about 72° for the main camera and about 110° for an ultra-wide.

## Run the test

Do this on Double Strip (about 30 yds to the line) and on Farm (100 to 120 yds) if you can, or anywhere with a few gates, trees or posts at known spots.

1. Press **Start** and allow camera, location and motion.
2. Hold the phone in landscape, level and still, at your normal height. Wait for GPS to settle (under about ±5 m) and press **Take photo**.
3. Tap two points on the guns' line (or a fence or hedge you know the distance to). Enter its distance in yards when asked.
4. Tap three to six things you can see at different distances and directions. Each tap shows its estimated distance. You can drag a mark to adjust it. Pinch with two fingers to zoom in on far ground and drag with one finger to move around; a single tap still places a mark. **Zoom out** returns to the whole photo.
5. Pace or measure the distance to each one and type it under **Paced yd** in **Results**. This is the most reliable check. For marks more than about 30 yds away you can also walk there and press **I'm here** (stand still for 5 seconds) to check the bearing with GPS. Closer than that, GPS error of about 5 yds swamps the result.
6. Read the table. "Dist. err yd" is how far the estimated distance was from your paced distance. "Miss yd" is how far the estimate was from where GPS put you. **Copy results** puts it on the clipboard so you can paste it back to me.

## What to look for

- **Bearing error.** Under about 5° is good. If every mark is off by the same amount, the compass is offset. If errors grow towards the edges of the photo, change the field of view in **Settings** until they shrink; that value is right for your phone.
- **Distance.** Compare the "level" estimate (from the phone's tilt alone) with the "guns' line" estimate. The plan expects the guns' line one to be much better, especially far out.
- **Miss yd.** If most misses are within about 10 to 15 yds at Double Strip distances and 25 to 30 yds on Farm, a dog working the area will find the bird and the photo method is worth building properly.
- **Handling.** Does marking in landscape with one hand feel natural? Is the photo clear enough in poor light?

## Known limits

- Assumes fairly flat ground between you and the mark. Slopes will show up as distance errors.
- Ignores sideways tilt of the phone; it warns if the photo was taken more than 4° off level.
- The field of view is a starting guess (70°) until you tune it.
- Built and tested for Chrome on Android. iPhone support is best effort.
