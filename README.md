# ACME Corp

Welcome to ACME. ACME is a fictional e-shop that sells Books and Appliances. In order to be successful in its endeavors it does what usual e-shop does:

- Purchases goods from vendors
- Sends Newsletters and advertises on multiple advertising platforms to attract traffic
- Follows its web performance
- Sells goods to end customers

## Intro to the task

Your task will be to create a table called Product Metrics. Product Metrics will be a single source of truth for the whole organization to understand performance of individual products. It will be used to answer business questions like:

- Which SKU has a negative margin?
- What is the source of traffic for this specific SKU?
- How much Adspend did we invest into specific brands?
- Is there a relationship between conversion rate and discount given?

## Prerequisite

Create a free project at https://www.keboola.com/ and load the data. Use this project to transform data and complete the tasks below.

## Your tasks

### Task 1

Create a table PRODUCT_METRICS according to this specification
Granularity: Year-Week-Source_Channel-SKU
Must have metrics:

- Adspend Cost per Product Detail View
- Product Purchase to Product Detail View Conversion rate
- Margin 3

Other Metrics and Attributes: which ever you will find useful to

- answer business questions above
- make it easy for user to understand your calculations

### Task 2

For table web_analytics create set of transformations that will regularly check quality of newly incoming data so you are alerted when something isn't right. Would it catch one glitch that happened in the past?

### Task 3

Data is coming from multiple sources. Do they provide same results? How would you solve the potential inconsistencies?

### What we are looking for

Your tasks will be evaluated against 2 criteria

a) Are your outputs logically and business-wise correct?

b) Is your code clear? Make sure that person unfamiliar with the topic can understand your logic. No need to impress us by overengineering.

## Data Available

### newsletters.csv

This is a datasource available from the mail sending platform (think Mailchimp). Contains information about newsletters sent, opened and clicked

### performance_marketing.csv

Colleague of yours was so nice to ingest data from various platforms so you know how much money was spent.

### webanalytics.csv

Data coming from Google Analytics. For weird reasons unknown to mankind ACME uses this source also for tracking items sold and its price.

### cogs.csv

This is how much the cost of the items was for ACME. It can change over time.

### bonuses.csv

This contains important info about back-margins. ACME collects additional money from vendors for services like better positioning on website, marketing services, connection to warehouse management and so on. These bonuses are negotiated at vendor level. Some bonuses are calculated as EUR per piece sold and some as % of COGS.

## Hints

SKU = Stock keeping unit. Individual product listed on website and sold to customers

P&L = Profit And Loss Statement;

| CATEGORY                  | Books     | Appliances | Comment                                                                              |
| ------------------------- | --------- | ---------- | ------------------------------------------------------------------------------------ |
| PIECES_SOLD               | 930882    | 19614      | Individual pieces sold                                                               |
| (+)REVENUE_EUR            | 20251319  | 3104476    | Price per piece x pieces sold                                                        |
| (-)COGS_EUR               | -18680919 | -3208137   | Costs of Goods Sold. Price that ACME pays to its vendors                             |
| (+)MARGIN_1               | 1570400   | -103661    | Sum of the above                                                                     |
| (+)BONUS_EUR_AS_PCT_COGS  | 3470761   | 642193     | Bonuses that are calculated as percentage of COGS.                                   |
| (+)BONUS_EUR_AS_PER_PIECE | 2792710   | 347807     | Bonuses that are calculated as EUR per piece.                                        |
| (+)MARGIN_2               | 7833872   | 886339     | Sum of the above                                                                     |
| (-)MARKETING_SPEND_EUR    | -556860   | -553718    | Amount that ACME pays to marketing platforms like Adwords and Facebook for campaigns |
| (+)MARGIN_3               | 7277012   | 332621     | Sum of the above                                                                     |

Do not worry about orchestrating the flow
