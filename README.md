# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where a server can hang due to long-running requests without proper asynchronous handling.  The `server.js` file contains the problematic code, causing the server to become unresponsive for 5 seconds during each request. The `serverSolution.js` file provides a corrected implementation using asynchronous operations and event loops to prevent the server from freezing. 

## Problem

The original code uses a synchronous `while` loop to simulate a long-running task. This blocks the Node.js event loop, preventing it from processing other requests or events.  The server appears to freeze, and no new connections can be established during this period.

## Solution

The solution utilizes asynchronous programming techniques.  This allows the server to remain responsive even when handling time-consuming tasks.  This prevents blocking the event loop and maintains server availability. 