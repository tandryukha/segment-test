# Segment Test Page

This repository contains a test page for the Segment proxy. It is used to verify that the proxy is working correctly by sending requests through it.

## Usage

1. Clone the repository:
   ```sh
   git clone git@github.com:tandryukha/segment-test.git
   ```

2. Open the `index.html` file in a browser or serve it using a local server.

3. Check the Network tab in DevTools to verify that requests are being routed through the proxy.

## Configuration

The `index.html` file is configured to use the Segment proxy for both CDN and API requests. The proxy URL is set to `https://segment-proxy.tandryukha.workers.dev`.

## GitHub Pages

This repository is hosted on GitHub Pages at [https://tandryukha.github.io/segment-test/](https://tandryukha.github.io/segment-test/).

## Playwright E2E Tests

This project uses Playwright for end-to-end testing of the Segment proxy. To run the tests:

1. Install dependencies:
   ```sh
   npm install
   ```

2. Run the tests:
   ```sh
   npm test
   ```

   This will run the tests in headless mode and auto-quit after completion.

3. For debugging, you can run the tests with the UI:
   ```sh
   npm run test:ui
   ```

4. To generate an HTML report:
   ```sh
   npm run test:report
   ```

The tests verify that:
- The Segment analytics.js script is loaded through the proxy.
- Tracking events are sent through the proxy.
- Identify calls are sent through the proxy. 