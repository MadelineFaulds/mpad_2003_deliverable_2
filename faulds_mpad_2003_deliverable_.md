**October 21, 2026**<br>
**MPAD2003A Introductory Data Storytelling**<br>
**Madeline Faulds**<br>
**Presented to Jean-Sébastien Marier**<br>

# Deliverable 2: Exploratory Data Analysis (EDA)

## Foreword

For this assignment, you must clean and analyze the dataset from Deliverable 1, create exploratory charts/visualizations, and identify a potential story. Your assignment must clearly detail your process. You are expected to write about 1,000-1,200 words, and to include several screen captures showing the different steps you went through. Your assignment must be written with the Markdown format and submitted on GitHub.

**Here are some useful resources for this assignment:**

* [GitHub's *Basic writing and formatting syntax* page](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
* [The template repository for this assignment in case you delete something by mistake](https://github.com/jsmarier/jou4100_jou4500_mpad2003_project2_template)

Did you notice how to create a hyperlink? In Markdown, we put the clickable text between square brackets and the actual URL between parentheses.

And to create an unordered list, we simply put a star (`*`) before each item.

## 1. Getting Data

I located the 2022, 2023, 2024, and 2025 datasets for the most requested titles at the Ottawa public Library, and downloaded each dataset in CSV format. I then entered an empty google sheet file, where I clicked file -> import, and uploaded the CSV files one at a time, and then imported the data. 

![](import-screen-capture-2022.png) <br> 
*Figure 1: The "Import File" prompt on Google Sheets for the 2022 dataset.*
![](import-screen-capture-2023.png) <br> 
*Figure 2: The "Import File" prompt on Google Sheets for the 2023 dataset.*
![](import-screen-capture-2024.png) <br> 
*Figure 3: The "Import File" prompt on Google Sheets for the 2024 dataset.*
![](import-screen-capture-2025.png) <br> 
*Figure 4: The "Import File" prompt on Google Sheets for the 2025 dataset.* 

I intend to compare these datasets to social media "reading lists" for the corresponding years, so I also located articles that listed the 2022, 2023, 2024, and 2025 most recommended titles on BookTok. I used `=IMPORTHTML("https://mashable.com/article/most-read-books-2022-tiktok", "list")` as it is the only list on the website. I used`=IMPORTXML("https://www.usmagazine.com/entertainment/news/2023-booktok-recommendations-biggest-books-on-the-app/", "//h3[contains(text(), 'by') or contains(text(), 'Happy Place')]")` for a 2023 list, which were all unfortunately much shorter, and the command filtered out the "related" pop ups. I used `=IMPORTXML("https://www.rollingstone.com/culture/culture-lists/booktok-best-books-2024-1235090973/piglet-by-lottie-hazel-1235203379/", "//h2")` for a 2024 list. And finally, I used `=IMPORTXML("https://www.kobo.com/blog/the-best-book-booktok-2025", "//h2")` for a 2025 reading list. 



## 2. Understanding Data

### 2.1. VIMO Analysis

Use three hashtag symbols (`###`) to create a level 3 heading like this one. Please follow this template when it comes to level 1 and level 2 headings. However, you can use level 3 headings as you see fit.

Insert text here.

Support your claims by citing relevant sources. Please follow [APA guidelines for in-text citations](https://apastyle.apa.org/style-grammar-guidelines/citations).

**For example:**

As seen in Bounegru & Gray (2011), a data visualization should be clear...

### 2.2. Cleaning Data

I selected the first 100 titles of each set, which I pasted into a new sheet (no longer attached to import). I deleted all of the unnesecary columns for my intended story, which were Collection, Catalogue, Format, FID, and Object ID. I froze the first row, and bolded the titles of each column for clarity. 

The 2025 dataset was not organized from most requested to least requested like the others, so I had to sort the sheet by column F (amount of holds) Z-A so that it would display the title with the most holds of 2025 as the first item. 

I used `=SPLIT(A1, "by", FALSE)` on the 2022 and 2023 BookTok reading list imports to separate the title and authors names into two different columns for clarity and consistency.

### 2.3. Analyzing Data

Insert text here.

**This section should include a screen capture of your pivot table, like so:**

![](pivot-table-screen-capture.png)<br>
*Figure 2: This pivot table shows...*

**This section should also include a screen capture of your exploratory chart, like so:**

![](chart-screen-capture.png)<br>
*Figure 3: This exploratory chart shows...*

## 3. Delivering Data

Insert text here.

## 4. References

Include a list of your references here. Please follow [APA](https://apastyle.apa.org/style-grammar-guidelines/references) or [MLA](https://www.mla.org/MLA-Style) guidelines for references. Hanging paragraphs aren't required though.

**Here's an example:**

Bounegru, L., & Gray, J. (Eds.). (2021). *The Data Journalism Handbook 2: Towards A Critical Data Practice*. Amsterdam University Press. [https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153](https://ocul-crl.primo.exlibrisgroup.com/permalink/01OCUL_CRL/hgdufh/alma991022890087305153)
