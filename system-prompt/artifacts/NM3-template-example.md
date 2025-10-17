<?xml version="1.0" encoding="UTF-8"?>
<!-- 
  NM3 Node Template - VALIDATED STRUCTURE
  Copy this exact pattern for every node generation
-->
<nm3 version="1.0">
  <meta title="Template" created="2025-10-17T00:00:00Z" />
  <camera position-x="0" position-y="5" position-z="10" 
          look-at-x="0" look-at-y="0" look-at-z="0" fov="75" />
  
  <nodes>
    
    <!-- TEMPLATE NODE 1 - MINIMAL -->
    <node id="node-1" type="sphere" x="0" y="0" z="0" 
          scale="1.0" color="pastel-blue">
      <title>Node Title</title>
      <content><![CDATA[
# Content Here

Your markdown content.
      ]]></content>
    </node>
    <!-- END NODE 1 - Notice the </node> closing tag above -->
    
    <!-- TEMPLATE NODE 2 - WITH ALL ELEMENTS -->
    <node id="node-2" type="cube" x="3" y="0" z="0" 
          scale="1.5" color="pastel-green">
      <title>Another Node</title>
      <content><![CDATA[
# More Content

Additional markdown here.
      ]]></content>
      <tags>example,template</tags>
    </node>
    <!-- END NODE 2 - Notice the </node> closing tag above -->
    
    <!-- TEMPLATE NODE 3 - SHOWS NESTING BOUNDARIES -->
    <node id="node-3" type="pyramid" x="-3" y="2" z="0" 
          scale="2.0" color="pastel-yellow">
      <title>Third Node</title>
      <content><![CDATA[
# Final Example

This shows proper structure.

Key points:
- Every <node> has </node>
- Every <content> has </content>
- CDATA opens with <![CDATA[
- CDATA closes with ]]>
      ]]></content>
      <tags>important</tags>
    </node>
    <!-- END NODE 3 - Notice the </node> closing tag above -->
    
  </nodes>
  <!-- ALL nodes must appear BEFORE this closing nodes tag -->
  
  <links>
    <link from="node-1" to="node-2" type="relates" />
    <link from="node-2" to="node-3" type="leads-to" />
  </links>
  
</nm3>

<!--
VALIDATION CHECKLIST FOR THIS TEMPLATE:
✓ 3 opening <node> tags
✓ 3 closing </node> tags
✓ 3 opening <content> tags
✓ 3 closing </content> tags
✓ 3 opening <![CDATA[ markers
✓ 3 closing ]]> markers
✓ All tags balanced
✓ Structure is well-formed XML

CRITICAL PATTERN TO REMEMBER:
<node ...>      ← Opening tag
  <title>...</title>
  <content><![CDATA[...]]></content>
  <tags>...</tags>
</node>         ← MUST have this closing tag

NEVER end a node without </node>
-->