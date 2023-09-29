```dataviewjs
let pg = dv.current();
dv.header(1,pg.file.name); //Header pliku brany z nazwy

let pages = dv.pages(`"${pg.file.folder}"`);
for (let page of pages)
{
	if(page.file.folder == pg.file.folder 
	&& !page.file.folder.contains(page.file.name))
	{    
		dv.paragraph("[["+page.file.name+"]]");
		let photo = "![["+page.file.name+" fota.jpg|300]]";
		let newPhoto = photo.replace("†", "");
		dv.paragraph(newPhoto);
	}
}
```
