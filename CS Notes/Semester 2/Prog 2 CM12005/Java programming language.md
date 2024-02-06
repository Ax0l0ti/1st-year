# The Java programming language
---
*Date :*  15-11-2023 
*Module :* #CM12005 
*Teacher*: 
*Resources :*

---
##### Contents: 
> [[#Inheritance]]
> [[#Polymorphism]]
> [[# ]]
> 
--- 

### Inheritance
>Inheritance allows the definition of classes as extensions of other classes. 

![[Pasted image 20221129112214.png | 500]]

Using these classes we can instantiate objects of the music and video files we own and add them to our database. 

For now our Music files may look like this
```Java
public class MusicFile{ 
	private String title ; 
	private String artist ; 
	private String comment; 
	public MusicFile(String theTitle, String theArtist) { 
		title = theTitle; 
		artist = theArtist; comment = ""; } 
	
	public void setComment (String newComment) {...} 
	public String getComment() {...} 
	public void print() {...} 
}
```
And our video files may look as such:
``` Java
public class Video{ 
	private String title ; 
	private String director ; 
	private String comment; 
	
	public Video(String theTitle, String theDirector) { 
		title = theTitle; 
		director = theDirector; comment = ""; 
	} 
	
	public void setComment (String newComment) {...} 
	public String getComment() {...} 
	public void print() {...} 
}
```

Using inheritance we can:
	- define one superclass - ITEM
	- define subclasses for video and musicFile
	- Superclass defines common attributes
	- The subclasses inherit the superclass attributes
	- The subclasses add own attributes

So we write the following code of the Item class (which will be our superclass):
```Java
public class Item{ 
	private String Title; 
	private int playingTime; 
	private boolean gotIt; 
	private String comment; 

	public Item(Sring theTitle, int time){ 
		title = theTitle; 
		playingTime = time; 
		gotIt = false; comment = ""; 
	} 
	public void print(){ ... } ... }
```

So let's say we want to inherit from the item class to the music file class:
```Java
public class MusicFile extends Item{ 
	private String artist; 
	private int numberOfTracks; 
	public MusicFile(String theTitle, String theArtist, int tracks, int time){
		super(theTitle, time);
		artitst = theArtist; 
		numberOfTracks = tracks; 
		} 
		... 
	}

```


### Polymorphism

Object variables in Java are polymorphic – they can hold objects of more than one type.
``` Java
Item item1 = new Item(...); 
Item item2 = new Video(...);
```
Polymorphism is where an object can take many different forms. 
