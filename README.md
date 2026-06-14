[Dribbble Designer Scraper](https://apify.com/easyapi/dribbble-designer-scraper?fpr=data)

# 🎨 Dribbble Designer Scraper

This Actor scrapes designer profiles from Dribbble based on a given keyword search. It utilizes Puppeteer with stealth mode to navigate through search results and extract detailed information about designers.

## ✨ Features

- 🔍 Search for designers using keywords
- 👤 Extract designer profiles including username, profile URL, and professional status
- 🛠️ Collect designer skills and meta tags
- 🔢 Configurable maximum number of results
- 🕵️ Uses stealth mode to avoid detection

## 📥 Input

The Actor accepts the following input parameters:

- `keyword` (required): The search term to find designers on Dribbble
- `maxResults` (optional): The maximum number of designer profiles to scrape (default: 100)

## 📤 Output

The Actor outputs a dataset containing the following information for each designer:

- 👤 Username
- 🔗 Profile URL
- 🏅 Professional status (PRO badge)
- 💼 Skills
- 🏷️ Meta tags

## 🚀 Usage

To use this Actor, simply provide a search keyword and optionally set the maximum number of results you want to scrape. The Actor will then navigate through Dribbble's search results, collecting designer information until it reaches the specified limit or exhausts all results.

This Actor is perfect for recruiters, design agencies, or researchers looking to gather information about designers with specific skills or specialties on Dribbble.

## 💡 Use Cases

- 🎯 Targeted Recruitment: Quickly find designers with specific skills
- 🔬 Market Research: Analyze trends in designer skills and popular tags
- 🤝 Partnership Discovery: Find potential freelancers or design agencies
- 🏆 Talent Tracking: Monitor top designers' activities and status

### Input Example

A full explanation of an input example in JSON.

```
{
  "maxResults": 100,
  "keyword": "ios"
}
```

### Output sample

The results will be wrapped into a dataset which you can always find in the **Storage** tab. Here's an excerpt from the data you'd get if you apply the input parameters above:

And here is the same data but in JSON. You can choose in which format to download your data: JSON, JSONL, Excel spreadsheet, HTML table, CSV, or XML.

```
[
	{
		"userName": "UI8",
		"profileUrl": "https://dribbble.com//UI8",
		"pro": "Pro",
		"skills": [
			"creative direction",
			"interaction design",
			"animation",
			"3d graphics",
			"branding",
			"ui",
			"web design",
			"product design",
			"ux"
		],
		"tags": [
			"From $20,000/project",
			"Dubai, United Arab Emirates",
			"Responds within a day"
		]
	},
	{
		"userName": "Vladimir Rakshâ",
		"profileUrl": "https://dribbble.com//rakshamann",
		"pro": "Pro",
		"skills": [
			"website design",
			"uiux design",
			"ios ui",
			"application",
			"landing",
			"app design",
			"ux design",
			"mobile design",
			"dashboard",
			"ui design",
			"web design",
			"web ui"
		],
		"tags": [
			"From $1,200/project",
			"United Arab Emirates",
			"Responds within a few hours"
		]
	},
    ...
]
```