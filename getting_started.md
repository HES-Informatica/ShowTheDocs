
Generate documentation using ShowTheDocs! it's pretty easy. Consider the following json:


content.json
```json 
{
    "title": "Show The Docs!",
    "description": "FlatFile Documentation Generator",
    "searchplaceholder": "Find me :)", // the placeholder text used for searchbox on top navbar. Default is search
    "datelabel": "Updated", // the text used before any article date. Default is empty
    "infolabel": "Info", // the text used as label on any info alert. Default is "Info"
    "warninglabel": "Warning", // the text used as label on any warning alert. Default is "Warning"
    "dangerlabel": "Danger", // the text used as label on any danger alert. Default is "Danger"
    "social": [ // generate top navbar and footer icons with links
        {
            "name": "Github",
            "icon": "fa fa-github", // any fontAwesome 6 Icon
            "url": "http://github.com/zonaro"
        }
    ],
    "logo": "https://place-hold.it/200x100?text=ShowTheDocs", // absolute path to your logo
    "downloadbutton": "http://github.com/zonaro/ShowTheDocs", //ommit if you want to hide download button
    "content": [
        {
            "id": "1", // needs to be unique. its also defines the hierarchy of articles
            "icon": "fas fa-file", // any fontAwesome 6 Icon
            "title": "Introduction", // article title
            "date": "05/05/2022",
            "contentfile": "https://raw.githubusercontent.com/yourusername/yourrepo/main/README.md", //needs to be absolute
            "aftercontentfile":"https://raw.githubusercontent.com/yourusername/yourrepo/main/LICENSE", //needs to be absolute
            "info": "this is a info alert",
            "danger": "this is a danger alert",
            "warning": "this is a warning alert",
            "lightbox": [ // creates a carroussel with images after content and before alerts and aftercontent
                {
                    "image": "https://raw.githubusercontent.com/yourusername/yourrepo/main/image.png", //needs to be absolute
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
            "title": "Sublevel 1.1"  
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