## Architecture

There are three parts to the eRegulations application: a parser that converts regulation text into data ([regulations-parser](https://github.com/cfpb/regulations-parser)), an API that hosts this data ([regulations-core](https://github.com/cfpb/regulations-core)), and a webapp which uses the data from the API to construct beautiful and usable regulations ([regulations-site](https://github.com/cfpb/regulations-site)).

One would typically run the parser against a regulation once (for each version) to populate the API with all the necessary data. regulations-site would then use regulations-core to as necessary to display regulations.


