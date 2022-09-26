
Generate documentation using `ShowTheDocs!` it's pretty easy. Create a GitHub repo with the following json on documentation branch an name it **content.json**:
 
```json 
{
    "language":"pt-BR",
    "title": "Show The Docs!",
    "description": "FlatFile Documentation Generator",
    "favicon":"https://place-hold.it/100x100?text=STD", // path to your favicon (absolute or relative to your GitHub Repo)
    "color":"#FFFF00", // CSS color. Used as accent color. Default is orange
    "author":"Your Name",
    "logo": "https://place-hold.it/200x100?text=ShowTheDocs", //path to your logo (absolute or relative to your GitHub Repo)
    "downloadbutton": "http://github.com/zonaro/ShowTheDocs", //ommit if you want to hide download button
    "printbutton": "Print Me", //ommit if you want to hide print button.
    "searchplaceholder": "Find me", // the placeholder text used for searchbox on top navbar. Default is "search"
    "datelabel": "Updated", // the text used before any article date. Default is empty
    "infolabel": "Info", // the text used as label on any info alert. Default is "Info"
    "warninglabel": "Warning", // the text used as label on any warning alert. Default is "Warning"
    "successlabel": "Warning", // the text used as label on any warning alert. Default is "Warning"
    "dangerlabel": "Success", // the text used as label on any success alert. Default is "Success"
    "viewraw": "Show File",// the text of file links (contentfile and aftercontentfile), ommit this property if you want to hide file links
    "copydialog": "CTRL+C to copy link",//  the text of copy dialog (for section anchors), ommit this property if you want to disable copy dialog and hide link icon
    "social": [ // generate top navbar and footer icons with links
        {
            "name": "Github",
            "icon": "fa fa-github", // any fontAwesome 6 FREE Icon
            "url": "http://github.com/zonaro"
        }
    ],
    "content": [
        {
            "id": "1", // needs to be unique. its also defines the hierarchy of articles
            "icon": "fas fa-file", // any fontAwesome 6 FREE Icon
            "title": "Introduction", // article title
            "date": "05/05/2022",
            "contentfile": "/README.md", // absolute url or relative to your GitHub Repo
            "aftercontentfile":"/LICENSE", // absolute url or relative to your GitHub Repo
            "info": "this is a info alert",
            "danger": "this is a danger alert",
            "warning": "this is a warning alert",
            "success": "this is a success alert",
            "lightbox": [ // creates a carroussel with images after content and before alerts and aftercontent
                {
                    "image": "/img/image.png", // image path, absolute or relative to your GitHub Repo
                    "title": "Image Description"
                }
            ]
        },
        {
            "id": "1.1", // set the id with sublevels to indicate that this article belongs to the previous article        
            "title": "Sublevel 1",           
            "content": "Lorem *Ipsum*...", //you can also use content instead of contentfile. Accepts markdown
            "aftercontent": "Lorem **Ipsum**..." //you can also use aftercontent instead of aftercontentfile. Accepts markdown
        },
        {
            "id": "1.1.1", // set the id with sublevels to indicate that this article belongs to the previous article         
            "title": "Sublevel 1.1.1"  
        },  
        {
            "id": "2", // set the id with sublevels to indicate that this article belongs to the previous article         
            "title": "Level 2"
        },
        {
            "id": "2.1", // set the id with sublevels to indicate that this article belongs to the previous article         
            "title": "Sublevel 2.1" 
        }
    ]
}
 
```

 