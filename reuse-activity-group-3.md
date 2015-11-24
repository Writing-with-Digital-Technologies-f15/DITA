# Content-Reuse Activity

## Group members

List your group members here. Delete this line.

- Lucy, Haiyen, Jacqui

## Questions about reuse practices

Answer the initial question by using the examples in this repo. Otherwise, use your books to answer the remaining questions. Be sure to integrate page number citations within each response.

1. _What content is being reused, if any, in the example topic models? What DITA reuse methods are being used? Write out the particular components with the syntax._
	
    The icecream and monkey examples reuse warning messages. The reuseable bits are identified with id attributes and then pulled into other dita files.
    
    **Initial ID:**
    ```xml
    <note id="mean">Monkeys are fun, but they can be mean! Be careful when handling monkeys.</note>
    ```
    
    **Reused:**
    ```xml
    <note conref="c_introduction.dita#cintro/mean"/>
    ```
    
2. _In your book, list out some general reuse cases in DITA._
	
    Can reuse: elements, topics, DITA maps, non-DITA content
    
3. _What are some good **phrase-level** conref practices?_
	
	- don't thoughtlessly put a conref in the middle of a sentence (issues with translation)
	- don't conref an entire sentence
	- if the only way to make a piece of content a conref is to use a <ph>, avoid conref
    - don't use too many conrefs in a single paragraph
    
4. _What are some good **topic reuse** practices?_
	- awareness of conref dependencies
	- avoid extensive/confusing dependencies
	- create conrefs only from files designated for reuse
    
5. _Define "spaghetti code" in relationship to conrefs._

	Spaghetti code is when files have extensive and confusing dependencies. Spaghetti code occurs when conrefs are used poorly.
    
6. _Define the <code>copy-to</code> attribute and write out an example case._
	
    Used when you have the same topic twice in a DITA map.
    ```xml
    <topicref href="action/create-testcase.dita" copy-to="action/1_create-testcase.dita"/>
    ```
    
    The book has an interesting example of <code>copy-to</code> use. (p. 193) Is this best use of the attribute? The example just slightly rephrases the link title, perhaps confusing the reader more than it helps the reader.
    
7. _Since we are not using a DITA-aware text editor, consider why an <code>id</code>-writing scheme will prove to be important. Come up with some rules of thumb for the class._
	
    DITA-aware text editors create the conref link for you automatically. Because we're not using a DITA-aware editor, id attributes will be the best way to create conref links.
    
8. _Consider how to integrate the reuse guidelines (pp. 199-200) into our writing and revision habits._
	
    Since our projects are relatively small, when we choose to use conrefs, we have to be careful that we are using them for the right reasons (aka, because they're useful, not just because we want to use the tag). Use id attributes carefully, as that will be our best way of linking to content. Avoid redundancy. 

