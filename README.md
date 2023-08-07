I have made a sql project on the topic 'Trade statistics of India for export and import of commodities from 2010-2021' taking the dataset from kaggel 
(kaggle datasets download -d lakshyaag/india-trade-data) 

number of countries in the dataset ?
-85306

Which are the top 5 trading partners for India?

select value
FROM trade
ORDER BY value DESC
LIMIT 5;

What are the major import categories for India ?

SELECT commodity, COUNT(value)  
FROM trade
ORDER BY value DESC
LIMIT 5;

What are the average prices or values of the major imported goods?

SELECT AVG(DISTINCT value)
FROM trade;
