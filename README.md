# Welcome to Jigx Snippets!

Here you can find a collection of snippets for the **Live Jigx Editor**.

## Structure

The **[samples](https://github.com/jigx-com/jigx-snippets/tree/main/samples)** folder contains different snippet categories. For now, there are three of them:

- [UI](https://github.com/jigx-com/jigx-snippets/tree/main/samples/ui)
- [Data](https://github.com/jigx-com/jigx-snippets/tree/main/samples/data)
- [Widgets](https://github.com/jigx-com/jigx-snippets/tree/main/samples/widgets)

Each category folder contains several samples. Not every file of these solutions will be editable in the Live Jigx Editor, but only those specified in the **contents.json** file in the root of this repository.

## contents.json

This file is the table of contents for the repository. The structure is:

    {
        snippets: [
    	    solutionPath: "samples/widgets/sample6/solution",
    	    snippetFilesPaths: [
    		    "samples/widgets/sample5/solution/jigs/todays-patient-plan.jigx"
    	    ],
    	    previewImgSrc: "samples/widgets/sample5/thumbnail.png",
    	    docUrl: "https://docs.jigx.com/docs/jw-group",
    	    category: "widgets"
        ]
    }

- **solutionPath** is a path to the solution folder.
- **snippetFilesPaths** is an array of the files which are supposed to be editable in the Live Jigx Editor.
- **previewImgSrc** is a path to the preview file. It is used for the snippet slider in the Live Jigx Editor.
- **docUrl** is a link to the documentation describing how to work with this snippet
- **category** is the snippet category. This field is used to populate categories in the Live Jigx Editor.

This is the essential file used by the **Live Jigx Editor**. It is parsed and used to display and load each snippet.

## Snippet files

The editable part of the snippet must be wrapped in the comments **#START_SNIPPET** and **#END_SNIPPET** as follows:

    title: Location widget
    type: jig.default
    children:
        - type: component.location
    		options:
    	    address: Narodni 135/14, 110 00 Praha
    #START_SNIPPET
    widgets:
    	4x2:
    		type: widget.location
    		options:
    			address: Narodni 135/14, 110 00 Praha
    #END_SNIPPET
