```dataviewjs
let pg = dv.current();
dv.header(1,pg.file.name + " ogólne");

let pages = dv.pages('"Postaci"');
for (let page of pages)
{
	if(page.file.folder == pg.file.folder && page.file.name != page.file.folder){  
		dv.paragraph("[["+page.file.name+"]]");
		let photo = "![["+page.file.name+" fota.jpg|300]]";
		let newPhoto = photo.replace("†", "");
		dv.paragraph(newPhoto);
	}
}
```
