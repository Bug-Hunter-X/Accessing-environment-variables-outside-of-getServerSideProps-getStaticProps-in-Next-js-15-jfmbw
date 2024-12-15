# Accessing environment variables outside of getServerSideProps/getStaticProps in Next.js 15

This repository demonstrates a common error encountered when working with environment variables in Next.js 15.

## Problem

Attempting to access environment variables directly within a page component (outside of `getServerSideProps` or `getStaticProps`) will result in an error.  This is due to the runtime environment differences between client-side rendering and server-side rendering.

## Solution

The solution involves moving the access to environment variables within either `getServerSideProps` or `getStaticProps`, ensuring that the data is available at build time or request time on the server.