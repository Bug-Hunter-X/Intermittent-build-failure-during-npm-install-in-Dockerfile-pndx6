# Intermittent Docker Build Failure

This repository demonstrates an issue where a Docker build intermittently fails during the `npm install` phase. The failure is non-deterministic, making it challenging to debug.

## Problem

The provided `Dockerfile` uses a Node.js base image and attempts to install dependencies using `npm`.  However, the build process sometimes fails with a non-zero exit code without providing clear error messages. This inconsistency makes it difficult to pinpoint the cause.

## Solution

The `Dockerfile.fixed` offers a potential fix. It includes a more verbose `npm install` command that outputs more detailed information during installation which aids debugging.