---
layout: default
title: "Arrange Code Snippets by Execution Flow"
---
## Task Instructions

In this task, you will organize code snippets to reconstruct the execution flow that answers a specific question about the code.

### What You Need to Do

1. **Identify Relevant Code**  
   - **Select only the code snippets** that contribute to answering the question.  
   - Ignore any lines that do not affect the actual execution flow.

2. **Arrange in Execution Order**  
   - **Drag and drop** the relevant snippets into the correct order.  
   - Ensure the sequence reflects the actual execution flow of the program.

3. **Ignore Distractors**  
   - Some snippets may appear relevant but are not part of the true execution.  
   - These should be **left out** of your final solution.

### How to Use the Interface

1. **Click "Start problem"**  
   This reveals the code blocks and begins timing your session.

2. **Construct Your Solution**  
   - Drag relevant snippets from the **Question Block** to the **Construct your solution here** area.  
   - You can rearrange or remove blocks as needed.

3. **Click "Check my answer"**  
   - Green blocks are correct and in the right order.  
   - Red blocks are either incorrect or out of order.

4. **Click "End problem"**  
   Once **all blocks under your solution are green**, click this to end the task.  
   Your **total time** and **number of attempts** will be recorded.

---

## Practice

<div id="sortableTrash" class="sortable-code" style="display:none></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="start" value="Start problem" type="button" />
    <input id="feedbackLink" value="Check my answer" type="button" /> 
    <input id="end" value="End problem" type="button" />
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "console.log(message);\n" +
    "const message = &quot;Hello, world!&quot;;\n" +
    "function showMessage() {\n" +
    "const sum = a + b #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#start").click(function(event){ 
      event.preventDefault(); 
      $("#sortableTrash").show();
  }); 
  $("#end").click(function(event){ 
      event.preventDefault(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  });
})(); 
</script>


## Task A: How do the provided props prevent scrolling when a modal is mounted?

<div id="p1-sortableTrash" class="sortable-code" style="display:none"></div> 
<div id="p1-sortable" class="sortable-code"></div> 
<div id="p1-log" style="display:none"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="p1-start" value="Start problem" type="button" />
    <input id="p1-feedbackLink" value="Check my answer" type="button" /> 
    <input id="p1-end" value="End problem" type="button" />
</p> 
<script type="text/javascript"> 
let p1Stats = 0;
let totalTimeP1;
(function(){
  var initial = "mount(modal: Modal, props: ManagedModalProps): void {\n" +
    "containerInfo.restore = handleContainer(containerInfo, props);\n" +
    "function handleContainer(containerInfo: Container, props: ManagedModalProps) {\n" +
    "if (!props.disableScrollLock) {\n" +
    "scrollContainer.style.overflow = &#039;hidden&#039;;\n" +
    "const restoreStyle = ownerDocument(container).querySelectorAll(&#039;.mui-fixed&#039;); #distractor\n" +
    "function setProperty(property: string, value: string | null, priority?: string) { #distractor\n" +
    "if (scrollElement.getAttribute(&#039;overflow&#039;) === &#039;auto&#039;) { #distractor\n" +
    "restoreStyle.forEach(({ value, scrollElement, property }) =&gt; { #distractor\n" +
    "scrollElement.style.setProperty(property, value); #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "p1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p1-start").click(function(event){ 
      event.preventDefault(); 
      totalTimeP1 = Date.now();
      $("#p1-sortableTrash").show();
  }); 
  $("#p1-end").click(function(event){ 
      event.preventDefault(); 
      totalTimeP1 = Date.now() - totalTimeP1;
      const seconds = (totalTimeP1 / 1000).toFixed(2);
      console.log("p1-time: ", seconds);
      $("#p1-log").text(`Task A — Total Time: ${seconds}s, Feedback Clicks: ${p1Stats}`);
      $("#p1-log").show();  
  }); 
  $("#p1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
      p1Stats += 1;
      console.log("p1: ", p1Stats);   
  }); 
})(); 
</script>

## Task B: How does the FocusTrap component handle focus restoration when it is closed?

<div id="p2-sortableTrash" class="sortable-code" style="display:none"></div> 
<div id="p2-sortable" class="sortable-code"></div> 
<div id="p2-log" style="display:none"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="p2-start" value="Start problem" type="button" />
    <input id="p2-feedbackLink" value="Check my answer" type="button" /> 
    <input id="p2-end" value="End problem" type="button" />
</p> 
<script type="text/javascript"> 
let p2Stats = 0;
let totalTimeP2;
(function(){
  var initial = "function FocusTrap(props: FocusTrapProps): React.JSX.Element { \n" +
    "const nodeToRestore = React.useRef&lt;EventTarget | null&gt;(null); \n" +
    "if (nodeToRestore.current &amp;&amp; (nodeToRestore.current as HTMLElement).focus) { \n" +
    "(nodeToRestore.current as HTMLElement).focus(); \n" +
    "let tabbable: ReadonlyArray&lt;string&gt; | HTMLElement[] = []; #distractor\n" +
    "const rootRef = React.useRef&lt;HTMLElement&gt;(null); #distractor\n" +
    "tabbable = getTabbable(rootRef.current!); #distractor\n" +
    "const lastKeydown = React.useRef&lt;KeyboardEvent | null&gt;(null); #distractor\n" +
    "lastKeydown.current?.shiftKey &amp;&amp; lastKeydown.current?.key === &#039;Tab&#039;, #distractor\n" +
    "if (nodeTabIndex === -1 || !isNodeMatchingSelectorFocusable(node as HTMLInputElement)) { #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "p2-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": false,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "p2-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p2-start").click(function(event){ 
      event.preventDefault(); 
      totalTimeP2 = Date.now();
      $("#p2-sortableTrash").show();
  }); 
  $("#p2-end").click(function(event){ 
      event.preventDefault(); 
      totalTimeP2 = Date.now() - totalTimeP2;
      const seconds = (totalTimeP2 / 1000).toFixed(2);
      console.log("p2-time: ", seconds);
      $("#p2-log").text(`Task B — Total Time: ${seconds}s, Feedback Clicks: ${p2Stats}`);
      $("#p2-log").show();
  }); 
  $("#p2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
      p2Stats += 1;
      console.log("p2", p2Stats); 
  }); 
})(); 
</script>
