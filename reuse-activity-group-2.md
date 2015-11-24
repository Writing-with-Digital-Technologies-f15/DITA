# Content-Reuse Activity

Please use this file-naming scheme: reuse-activity-group-[enter assigned # here].md. 

Save this file within the root DITA folder.

## Group members

List your group members here. Delete this line.

- matt
- anna
- alex

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

### 1. What content is being reused, if any, in the example topic models? What DITA reuse methods are being used? Write out the particular components with the syntax.

ex.: monkey DITA, `<note conref="c_introduction.dita#cintro/mean"/>`

### 2. In your book, list out some general reuse cases in DITA.

If you want to reuse product names or other common objects and things: references, topics, maps, and sources. These things can all be reused so that any changes will propogate to all places where that content has been reused.

### 3. What are some good **phrase-level** conref practices?

Don't reuse everything because it could complicate translation processes; reuse phrase-level topics only when referencing proper nouns like product/model names

### 4. What are some good **topic reuse** practices?

Reuse topics when they contain boilerplate text like legal text and stuff. Reuse task topics when the same procedure is repeated several times in different contexts.

### 5. Define "spaghetti code" in relationship to conrefs.

Code that is complex and has tangled control structure. Basically it doesn't make sense and structured conrefs help to detangle the spaghetti.

### 6. Define the <code>copy-to</code> attribute and write out an example case.

<code>copy-to</code> is used when you want to duplicate a topic, but don't want to actually duplicate the source file. This could a

```
<topicref href="file.dita" copy-to="copy_file.dita">
  <topicmeta>
    <linktext>title one</linktext>
  </topicmeta>
</topicref>
```

### 7. Since we are not using a DITA-aware text editor, consider why an <code>id</code>-writing scheme will prove to be important. Come up with some rules of thumb for the class.

Good <code>id</code>-writing schemes are important because in order to properly place tags for topic reuse, we'll semantic id values so we can tell what is supposed to go where and how it fits into context. For example, when we want to reuse a topic for a model name, its id might be <code>"model_name"</code>

### 8. Consider how to integrate the reuse guidelines (pp. 199-200) into our writing and revision habits.

