---
layout: default
title: "Arrange Code Snippets by Execution Flow"
---
## Task Instructions

1. **Identify Relevant Code**  
   - **Select only the code snippets** that contribute to answering the question.
   - Ignore any snippets that do not affect the actual execution flow.

2. **Arrange in Execution Order**  
   - **Drag and drop the selected snippets** to reorder them so they reflect the true execution order.
   - Ensure that the sequence mirrors the flow of the underlying program logic.

3. **Ignore Distractors**  
   - Some snippets may appear relevant but are not part of the actual execution.  
   - These distractors should be **excluded** from your final solution.

---

## Task A: How do the provided props prevent scrolling when a modal is mounted?

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
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
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

## Task B: How does the FocusTrap component handle focus restoration when it is closed?

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
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
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
