# Content-Reuse Activity

Please use this file-naming scheme: reuse-activity-group-1.md.

Save this file within the root DITA folder.

## Group members

- Mao Thao, John Buckeye, Andrew Burke

## Questions about reuse practices

**Note**: You can cite longer snippets of code by using markdown's code syntax highlighting like this:

```xml
<steps>
	<step>
		<cmd>Locate source materials</cmd>
	</step>
	<step>
		<cmd>Gather the evidence</cmd>
	</step>
	<step>
		<cmd>Write out the answer</cmd>
	</step>
</steps>
```

Answer the initial 2 questions by using the examples in this repo. Otherwise, use your books to answer the remaining questions. Be sure to integrate page number citations within each response.

<<<<<<< HEAD
### 1. What content is being reused, if any, in the example topic models?  What DITA reuse methods are being used? Write out the particular components with the syntax.
t_fix.dita and t_clean.dita. They linked to a warning page to turn off the machine prior to doing the task with a <conref> tag.

### 2. In your book, list out some general reuse cases in DITA.
You can reuse content you are working with similar products or tasks with the same steps.
=======
### 1. What content is being reused, if any, in the example topic models? What DITA reuse methods are being used? Write out the particular components with the syntax.


### 2. In your book, list out some general reuse cases in DITA.


### 3. What are some good **phrase-level** conref practices?


### 4. What are some good **topic reuse** practices?


### 5. Define "spaghetti code" in relationship to conrefs.


### 6. Define the <code>copy-to</code> attribute and write out an example case.
>>>>>>> ee7bfdd8eede4df1332f7928b5d03970ffb6b787

### 3. What are some good **phrase-level** conref practices?
Use the <copy-to> attribute when necessary
Don't write additional elements just to reuse

<<<<<<< HEAD
### 4. What are some good **topic reuse** practices?
Designated source topics
Design and adhere to a file hierarchy
=======
### 7. Since we are not using a DITA-aware text editor, consider why an <code>id</code>-writing scheme will prove to be important. Come up with some rules of thumb for the class.
>>>>>>> ee7bfdd8eede4df1332f7928b5d03970ffb6b787

### 5. Define "spaghetti code" in relationship to conrefs.
Topics link to other topics without organization, leaving the reader lost. One topic might be linked to as well as linked from, rather than being designated one or the other.

<<<<<<< HEAD
### 6. Define the <code>copy-to</code> attribute and write out an example case.
This is an attribute which creates one path from a topic which might have multiple links to the same re-used content. This might happen when such content needs to be importantly linked again, such as an overviewed product, and then a sub-product which perfectly fits that content.

### 7. Since we are not using a DITA-aware text editor, consider why an <code>id</code>-writing scheme will prove to be important. Come up with some rules of thumb for the class.
This would create the same networking possiblities which such a text editor might already have. In this way, there would be a smooth transition if the conref itself needs to be switched, or you need to add a conref very quickly to something you may not have anticipated having to link to.

### 8. Consider how to integrate the reuse guidelines (pp. 199-200) into our writing and revision habits.
We can each do what we feel, but there might be a solid reason to not go too "small" in the size elements you allow yourself to re-use. Find which content is suitable for re-use, create your ids and keep those at about the same level of the hierarchy.
=======
### 8. Consider how to integrate the reuse guidelines (pp. 199-200) into our writing and revision habits.
>>>>>>> ee7bfdd8eede4df1332f7928b5d03970ffb6b787
