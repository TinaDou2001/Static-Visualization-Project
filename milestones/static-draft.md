# U.S. Food Imports

Tina Dou

## What is your current goal? Has it changed since the proposal?

My current goal is to create a compelling narrative about U.S. food import patterns, with a specific focus on consumer trends and category-level analysis. While my original proposal looked at overall food imports, I've refined my focus to drill down into specific food categories like meats, beverages, and produce to tell more engaging stories about American consumption habits. I want to move beyond generic overall trends and explore questions like: What types of meat does America import most? How have beverage preferences changed over time? Which countries specialize in exporting specific food categories to the U.S.?

## Are there data challenges you are facing? Are you currently depending on mock data?

I'm facing one significant data challenge that I plan to address before the final submission: data duplication in commodity categories. The dataset contains both aggregate categories (like "Total live animals") and their subcomponents, which means some visualizations may be double-counting values. For example, "Total live animals" likely includes all the individual animal categories beneath it. I'm currently using the raw data but will need to filter out these aggregate categories to ensure accurate analysis. This is particularly important for charts that show composition or market share.

## Describe each of the provided images with 2-3 sentences to give the context and how it relates to your goal.

![](mock_visualizations/visualization1.png)

This chart shows how the total value of U.S. food imports has changed from 1999 to 2024. 
Each point represents one year’s total import value (in millions of dollars), connected by a teal line to highlight overall growth. 
The steady upward trajectory reflects both increasing global trade volumes and rising food prices. 
This serves as an opening overview in my narrative, establishing the scale and long-term upward trend before examining what commodities and partner countries drive that growth.

![](mock_visualizations/visualization2.png)

This stacked area chart builds directly on the first visualization. 
While the first figure showed the total growth of food imports, this one decomposes that growth by category. 
Each band’s thickness represents the total dollar value of that category in a given year. 
The chart reveals that imports have not only increased overall but that some categories have expanded more rapidly than others. 
Keeping the scale in raw dollar terms emphasizes both the magnitude of import growth and the changing composition of the U.S. food supply.

![](mock_visualizations/visualization3a.png)
![](mock_visualizations/visualization3b.png)

The next two bar charts identify the countries that supply the greatest total value of food imports to the United States. 
Each bar’s height corresponds to the cumulative import value in millions of dollars, sorted from largest to smallest. 
Canada and Mexico dominate, reflecting the importance of North American trade under long-standing agreements such as NAFTA/USMCA, while countries such as China contribute smaller but significant shares. 
This visualization follows the previous two by shifting the focus from overall trends to the global origins of those imports, setting the stage for later charts that explore regional patterns and specific commodities.

What seems interesting to me is that Italy is in the top 3, making me wonder what it actually exports to America?

![](mock_visualizations/visualization4.png)

This choropleth map uses geographic shading to display where U.S. food imports originate. 
Each country’s color corresponds to the total dollar value of food exported to the United States, with deeper red hues indicating larger trade volumes. 
The map highlights North American partners such as Canada and Mexico as the dominant exporters, while other regions appear lighter, reflecting smaller shares or missing data.

To construct the map, I first reviewed Altair’s documentation on mark_geoshape() but struggled with the data-merging step needed to join import totals with country geometries. 
I consulted ChatGPT for guidance on performing that merge correctly with GeoPandas and Altair. 
Although the final visualization works as intended, I am personally not a big fan of it—the dataset includes a limited number of countries, which reduces the richness of the spatial comparison. 
Nevertheless, it contributes a useful geographic perspective to my overall narrative.

![](mock_visualizations/visualization5.png)

This donut chart displays the proportion of total U.S. food import value accounted for by each major category. 
The angle of each wedge corresponds to its share of total import spending, while color differentiates categories. 
The visualization provides a compact overview of how U.S. food imports are distributed across sectors such as animal products, plants, and processed foods. 
It helps transition from the earlier time-series visualizations to a static summary of relative importance.

I considered creating a stacked bar chart instead but chose a donut because it communicates overall proportions more directly. 
While pie-style visuals are not ideal for precise comparison, they work well here to show the dominance of certain broad categories.

![](mock_visualizations/visualization6.png)

This stacked percentage area chart shows how different food categories’ shares of total U.S. imports have evolved over time. 
Each band’s height represents its proportional contribution to total import value for that year, normalized to 100%. 
The use of normalized stacking highlights shifts in composition whether certain categories are gaining or losing share—rather than changes in absolute size.

I chose this format to emphasize structural change instead of total volume, since previous charts already captured overall growth. 
This chart reveals which sectors expanded or declined in importance over the years and provides a more balanced comparison between categories of very different scales.

![](mock_visualizations/visualization7.png)

This visualization displays each food category’s import trend over time using a set of small multiple line charts. 
Each panel focuses on one category, allowing direct comparison of patterns across sectors while preventing the largest categories from overpowering the smaller ones. 
The combination of line and point marks makes year-to-year fluctuations easy to follow.

I chose the faceted design to make structural patterns clearer — for example, which categories show steady growth versus volatility. 
It complements the earlier stacked percentage chart by presenting the absolute trends behind the relative shares, offering a detailed, category-level perspective within the overall import system.

![](mock_visualizations/visualization8.png)

The size of each circle reflects total import value, while color intensity corresponds to the number of commodities within that category. 
Although the encoding captures multiple dimensions simultaneously, I found the result difficult to interpret because of visual clutter and overlapping points. 
The bubbles make it hard to extract a clear pattern compared with previous visualizations.

I included this chart as an experimental design to explore whether combining “value” and “diversity” in one space could highlight interesting relationships, 
but in practice it reinforced the importance of prioritizing readability and single-variable clarity in future iterations.
Tip: The markdown syntax ![](image-name.png) will let you embed images directly, or you can number them and describe them by number in this file.

## What form do you envision your final narrative taking? (e.g. An article incorporating the images? A poster? An infographic?)

An article incorporating the images.