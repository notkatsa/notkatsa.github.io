---
layout: post
title: "Price monitor"
date: 2024-11-26
---
# Documenting the Creation of the Price monitor

## Introduction

Creating a price monitor for dynamically loaded web pages was a fascinating challenge, requiring a blend of modern web scraping tools like Selenium and BeautifulSoup. The goal was simple but ambitious: to find the minimum price of various products across several pages and notify users of any price changes. Here's a look at the process, the obstacles faced, and how ChatGPT-4o with canvas made the journey far smoother than anticipated.

## The Development Journey

The initial version of the monitor was straightforward—using Selenium to navigate product pages, extracting the HTML, and BeautifulSoup to parse the content. However, complications arose when we realized that many pages load prices dynamically and reorder the elements each time the page loads. It wasn't just about extracting a price but making sure that we found the correct, lowest price efficiently.

To add complexity, scraping had to be scaled to multiple URLs, each with unique layouts and loading patterns. We integrated delays to mimic human behavior, preventing the bot from being blocked by anti-scraping measures.

### Challenges Faced

1. **Dynamic Loading**: Product pages were dynamically loaded, requiring careful handling to ensure the entire content was available before parsing. This led to experimenting with waiting times and explicit waits in Selenium.
2. **Inconsistent HTML Structure**: The order of elements within the scraped HTML varied between requests, which meant our initial approach of finding the first price element was unreliable. We adjusted the monitor to collect all prices and determine the lowest among them.
3. **Scaling and Efficiency**: Scaling from one URL to multiple URLs brought its own set of challenges. Each page had to be scraped individually, with sufficient delays to avoid being blocked.
4. **Notifying Users**: We implemented system notifications using the `plyer` library to alert users when a product price changed from the previous check. This added real-time utility, making the tool genuinely valuable.

## Timeline

The entire process took approximately two hours to complete, partially due to ChatGPT-4o with Canvas.

### My praises to ChatGPT-4o with Canvas

A huge part of the credit goes to ChatGPT-4o with canvas for making this development possible. The interactive editing and guidance provided throughout the process turned complex issues into manageable steps. Whether it was refining code for handling dynamic content or suggesting optimizations, ChatGPT-4o's assistance was instrumental in making this project a success.

## Potential Uses for This Tool

This price monitor has applications beyond personal use. Many online retailers or small e-commerce operators can use this tool to monitor competitors' prices and adjust their own pricing dynamically. 

For shop owners, this tool provides a competitive edge by allowing them to stay informed of competitor pricing without having to manually check each product. Automated price adjustments or promotional notifications can also be implemented on top of this monitor for greater business agility.

## Monetization Plan

The plan for monetization revolves around offering this tool as a subscription service to e-commerce businesses. Retailers and small businesses can subscribe to get daily price updates on their competitors' products.&#x20;

Given the growing demand for real-time market intelligence in e-commerce, this tool has great potential as a subscription-based solution. It can also be extended into a browser extension or mobile app for easier use by individual customers.

##

