# Blitz 1

## Purpose:
The purpose of this blitz test was to assess how our server would handle higher volume on the server. We will also identify opportunities to decrease server latency and enhance the overall user experience.

## Problem:
Once the application was subjected to traffic, specifically 1000 additional requests, the average latency climbed to approx. 40.8 ms. To address the issue of increased latency and maintain the user experience, we would implement the use of Cloudfront (Content Delivery Network).

## Implementing Cloudfront

1) Create a CloudFront distribution
2) Input origin domain (removed the backslash)
3) Create a Cache Policy that fits your needs. For this assignment, I used Caching Optimized
4) Click on Create Distribution

Once, you create a distribution, it will give you another URL that allows access to the website/ application with the implementation of Cloudfront. Cloudfront will start distributing content closer to the end user, reducing the load of traffic to the server, as well as, caching frequently accessed content. This in turn will reduce latency to approx 9 ms and increase the efficiency of the server.

## Cloudfront System Design
The view the system design for Cloudfront, click [here!](https://github.com/auzhangLABS/Blitz_Test_1/blob/main/cloudfront.diagram.png)

## Optimization:
To optimize this, I would implement a way to monitor your server (Amazon Cloudwatch or Datadog) and set a threshold. Once exceeds the threshold it will alert you or set up CloudFront automatically. This way, this process can be automated.
