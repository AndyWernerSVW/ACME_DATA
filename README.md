# ACME Corp

Welcome to ACME. ACME is a ficitional e-shop that does sells Books and Appliances. In order to be succesfull in its endeavours it does what usual e-shop does:

- Purchases goods from vendors
- Sends Newsletters and advertises on multiple advertising platforms to attract traffic
- Follows its web performance
- Sells goods to end customers

## Intro to the task

You task will be to create table called Product Metrics. Product Metrics will be a single source of truth for the whole organization to understand performance of individual products. It will be used to answer business questions like:

- Which SKU have negative margin?
- What is source of traffic for this specific SKU?
- How much Adspend did we invest into specific brands?
- Is there a relationship between conversion rate and discount given?

## Prerequisite

Create free project at https://www.keboola.com/ and load the data. Use this project to transform data and complete task below.

## Your task

Create table PRODUCT_METRICS according to this specification
Granularity: Year-Week-Source_Channel-SKU
Must have metrics:

- Adspend Cost per Product Detail View
- Product Purchase to Product Detail View Conversion rate
- Margin 3
  Other Metrics and Attributes: which ever you will find useful to
- answer business questions above
- make it easy for user to understand your calculations

## Hints

SKU = Stock keeping unit. Individual product listed on website and sold to customers

P&L = Profit And Loss Statement;

Do not worry about orchestrating the flow
