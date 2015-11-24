# Content-Reuse Activity

Please use this file-naming scheme: reuse-activity-group-[enter assigned # here].md. 

Save this file within the root DITA folder.

## Group members

List your group members here. Delete this line.

- Linus Chan

- Sarah Murto


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

### 1. What content is being reused, if any, in the example topic models?

## Conref Reuse

#### examples/monkeydita/t_feeding.dita 
```xml
<cmd>Serve food cold. Monkeys do not like hot food</cmd>
<info><note conref="c_introduction.dita#cintro/mean"/>
</info>
```


### examples/monkeydita/t_dancing.dita 
```xml
<cmd>Start the music and let the magic happen</cmd>
<info>
<note conref="c_introduction.dita#cintro/mean/>
</info>```

### examples/icecream/t_fix.dita 
```xml 
<cmd>Open the machine by kicking its right side.</cmd>
<info>
<p conref="c_welcome.dita#welcome/warning"/>
</info>
```


#### examples/icecream/t_clean.dita 
```xml
<cmd>Prepare the machine</cmd>
<info>
<p conref="c_welcome.dita#welcome/warning"/>
</info>
</step>
```

## Map Reuse

### css-grids/_supermap.ditamap

```xml
<topicref href="_bootstrap3.ditamap" format="ditamap">
<topicmeta>
<navtitle>Bootstrap 3 Grid</navtitle>
</topicmeta>
</topicref>
```

### 3. In your book, list out some general reuse cases in DITA.

-Warnings
-Instructions
-Product Names
-Menu labels
-Legal information
-Addresses
-Error messages
-Reference Material


### 4. What are some good **phrase-level** conref practices?

Avoid referencing content already referenced within a conref target (ditawriter.com)

Don't reuse a phrase from the middle of the paragraph. If you need to use a ph-tag to create the reuseable content, most likely you don't need to use it. (190)

Use phrase level for proper nouns or frequently changing content (200)



### 5. What are some good **topic reuse** practices?
WRite topics that'll make sense when taken out of content.

Include organizational features that make content east to scan and reuse elsewhere.

Don't use relational language (pointers)

Write componentized content that is feature-based so it can be reused (196)


Rewrite to make more generic (197)



### 6. Define "spaghetti code" in relationship to conrefs.

Multiple layers that point to multiple conrefs on multiple maps. (ditawriter.com)

Use an information architecture tool or other plan to make sure references don't come from all over the place. 

### 7. Define the <code>copy-to</code> attribute and write out an example case.

The copy-to attribute of the topicref element is used in the unusual situation where you need to create two copies of the same topic in the output, and to link to each copy of the output topic separately. 

<topicref href="oxygen.dita" copy-to="oxygen_turbo.dita">
  <topicmeta>
    <linktext>Oxygen Explained</linktext>
  </topicmeta>
</topicref>

(https://www.oxygenxml.com/dita/styleguide/webhelp-feedback/Artefact/Maps/c_copy-to_Attribute.html)


### 8. Since we are not using a DITA-aware text editor, consider why an <code>id</code>-writing scheme will prove to be important. Come up with some rules of thumb for the class.

When naming id codes make sure the ID fixs the context of the content.



### 9. Consider how to integrate the reuse guidelines (pp. 199-200) into our writing and revision habits.

Construct frameworks and maps at the start of your project.

Figure out what tasks you're tackling. Reference topics can then support these tasks. Look over your tasks with a fresh pair of eyes and look for overlaps every time you make a change, then link things together.

 


