# Node.js Server Unresponsiveness Due to Blocking Operation

This repository demonstrates a common issue in Node.js where a server becomes unresponsive due to a long-running synchronous operation blocking the event loop.  The `server.js` file shows the problematic code, while `serverSolution.js` provides a solution using asynchronous techniques.

## Problem

The server in `server.js` performs a computationally intensive task (a large loop) synchronously within the request handler. This blocks the event loop, preventing the server from processing other requests and leading to unresponsiveness.

## Solution

The `serverSolution.js` file demonstrates how to fix the problem by using asynchronous techniques.  In this case, even though we still simulate a long process, it is structured in a way that avoids blocking the event loop and allows the server to remain responsive.