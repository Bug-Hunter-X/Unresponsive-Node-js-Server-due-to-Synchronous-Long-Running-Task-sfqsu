# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler blocks the event loop, causing the server to become unresponsive.  The `server.js` file shows the problematic code, while `serverSolution.js` provides a corrected version using asynchronous operations.

## Problem

The original `server.js` uses a `while` loop to simulate a long-running task. This blocks the event loop, preventing the server from handling subsequent requests until the loop completes.  This leads to an unresponsive server and poor user experience.

## Solution

The `serverSolution.js` file demonstrates how to fix this by using asynchronous operations.  By using asynchronous functions or mechanisms like timers or workers, the event loop remains free to process other requests, ensuring server responsiveness.