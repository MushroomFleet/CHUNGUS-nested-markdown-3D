# NM3 Pre-Flight Validation Checklist

## MANDATORY: Execute Before Every Output

### Phase 1: Structure Counting
```
Count in your generation:
- Number of <node> opening tags: ___
- Number of </node> closing tags: ___
- MUST BE EQUAL
```

### Phase 2: Nested Element Verification
```xml
Every node MUST follow this exact pattern:

<node id="..." type="..." x="..." y="..." z="..." color="..." scale="...">
  <title>...</title>
  <content><![CDATA[
...
  ]]></content>
  <tags>...</tags>
</node>

CHECK:
â˜ Opening <node> tag has all required attributes
â˜ <title> element present and closed
â˜ <content> element present and closed
â˜ CDATA section properly opened with <![CDATA[
â˜ CDATA section properly closed with ]]>
â˜ <tags> element present and closed (if included)
â˜ Closing </node> tag present
```

### Phase 3: Common Error Patterns to AVOID

#### âŒ WRONG - Missing closing node tag:
```xml
<node id="test" type="sphere" x="0" y="0" z="0">
  <title>Test</title>
  <content><![CDATA[Content]]></content>
<!-- MISSING </node> HERE -->

<node id="test2" ...>
```

#### âœ… CORRECT - Properly closed:
```xml
<node id="test" type="sphere" x="0" y="0" z="0">
  <title>Test</title>
  <content><![CDATA[Content]]></content>
</node>

<node id="test2" ...>
```

#### âŒ WRONG - Self-closing node with content:
```xml
<node id="test" type="sphere" x="0" y="0" z="0" />
  <content><![CDATA[Content]]></content>
</node>
```

#### âœ… CORRECT - Full element form:
```xml
<node id="test" type="sphere" x="0" y="0" z="0">
  <content><![CDATA[Content]]></content>
</node>
```

#### âŒ WRONG - Unclosed CDATA:
```xml
<content><![CDATA[
# Some content
</content>
```

#### âœ… CORRECT - Properly closed CDATA:
```xml
<content><![CDATA[
# Some content
]]></content>
```

### Phase 4: Final XML Well-Formedness Check

Before output, verify this hierarchy is intact:

```
<?xml version="1.0" encoding="UTF-8"?>
<nm3 version="1.0">
  <meta ... />
  <camera ... />
  <nodes>
    <node ...>
      ...
    </node>  â† Every opening node MUST have this
    <node ...>
      ...
    </node>  â† Every opening node MUST have this
  </nodes>  â† This closes the nodes container
  <links>
    ...
  </links>
</nm3>
```

### Phase 5: Tag Balance Verification

Mental execution before output:
```
1. Scan for all "<node" strings â†’ Count = N
2. Scan for all "</node>" strings â†’ Count = M
3. IF N â‰  M â†’ ERROR: Fix immediately
4. Scan for all "<content>" â†’ Count = X
5. Scan for all "</content>" â†’ Count = Y
6. IF X â‰  Y â†’ ERROR: Fix immediately
7. Scan for "<![CDATA[" â†’ Count = A
8. Scan for "]]>" â†’ Count = B
9. IF A â‰  B â†’ ERROR: Fix immediately
```

### Phase 6: Automated Self-Correction Protocol

If any check fails:
1. **STOP generation immediately**
2. **Identify the unclosed tag**
3. **Insert proper closing tag**
4. **Re-run all checks**
5. **Only output after ALL checks pass**

### Emergency Recovery Template

If you detect an error during generation, use this recovery:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<nm3 version="1.0">
  <meta title="Recovery Mode" created="2025-10-17T00:00:00Z" />
  <camera position-x="0" position-y="5" position-z="10" 
          look-at-x="0" look-at-y="0" look-at-z="0" fov="75" />
  <nodes>
    <node id="error-recovery" type="sphere" x="0" y="0" z="0" 
          scale="2" color="pastel-pink">
      <title>XML Structure Error Detected</title>
      <content><![CDATA[
# Error Recovery Mode

An XML structure error was detected during generation.
Please review the input and try again.

Error type: Unclosed node element
      ]]></content>
      <tags>error,recovery</tags>
    </node>
  </nodes>
  <links></links>
</nm3>
```

## Critical Reminders

1. **EVERY `<node>` must have exactly ONE `</node>`**
2. **EVERY `<content>` must have exactly ONE `</content>`**
3. **EVERY `<![CDATA[` must have exactly ONE `]]>`**
4. **Count tags as you generate - if counts don't match, STOP and fix**
5. **Self-closing `<node />` is NOT valid when content is needed**

## Validation Commands (Mental Execution)

```
BEFORE OUTPUT:
- grep_count("<node") == grep_count("</node>") â†’ MUST BE TRUE
- grep_count("<content>") == grep_count("</content>") â†’ MUST BE TRUE  
- grep_count("<![CDATA[") == grep_count("]]>") â†’ MUST BE TRUE
- ALL nodes appear between <nodes> and </nodes> â†’ MUST BE TRUE
```

**DO NOT OUTPUT XML UNLESS ALL CHECKS PASS**