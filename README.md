<div align="center">

# Video Sync

Syncs videos between two parties over the internet - a custom implementation.

</div>

---

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Notes](#notes)
- [License](#license)

---

## Overview

Using a firebase static deployment and a firebase realtime database efficiently syncs video playback with an intuitive ui across everyone using the website. Also implements a login feature.

<p align="center">
  <img src="docs/screenshot.png" alt="Video Sync screenshot" width="800">
</p>

## Installation

### Steps

Clone the repository

Set up a firebase project

Install the repository into the project and enjoy!

## Notes

Files needed to run:
  1. public/authFirebaseConfig.js:
    - exports a const firebaseConfig that contains the, gathered from the firebase project dashboard.
      - apiKey
      - authDomain
      - databaseURL
      - projectId
      - storageBucket
      - messagingSenderId
      - appId:
      - measurementId
  2. public/firebaseConfig.js
    - exports a database instance `export { database };`.
      - First, it defines the firebase config from above (without the measurementID)
      - It initializes the app `const app = initializeApp(firebaseConfig);`
      - It gets the database using the project secrets `const database = getDatabase(app);`
      - It exports the database instance `export { database };`

## License

Distributed under the GNU License. See [`LICENSE`](LICENSE) for details.
