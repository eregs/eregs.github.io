### Architecture

There are three primary parts to the eRegulations application: a parser that converts regulation text into data (**regulations-parser**), an API that hosts this data (**regulations-core**), and a webapp which uses the data from the API to construct beautiful and usable regulations (**regulations-site**).

One would typically run the parser against a regulation once (for each version) to populate the API with all the necessary data. **regulations-site** would then use **regulations-core** as necessary to display regulations.