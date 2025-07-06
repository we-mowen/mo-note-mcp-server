# Mowen MCP Server

**Mowen** is an intelligent note-taking tool and content community that integrates recording, creation, and sharing, enabling valuable content to flow between people.

**Mowen MCP Server** provides capabilities such as note creation, editing, permission settings (public/private), and file uploads. By integrating with the Mowen MCP Server, users can write, refine, proofread, and directly save notes to the Mowen note tool using natural language on any MCP Host that supports [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) (such as Cursor, Trae, etc.).

| Version | v0.1.0        |
| ------- | ------------- |
| Description | Manage Mowen notes via MCP |
| Category    | Note        |
| Tags        | Text, Document Management, Note |

## Tools

This MCP Server provides the following tools:

### Tool 1: CreateRichNote

**Description:**  
Create a Mowen note supporting rich text formats, including **bold**, ==highlight==, [links](#), blockquotes, internal notes, images, audio, PDFs, and more.

**Prompt Example:**
```
"Beijing is so hot today" — create a Mowen note and tell me the note ID.
```
```
Read the @note.md document, create a Mowen note (do not make it public). Properly segment the document, add spaces between Chinese and English, and use bold/highlight for key terms to make the format beautiful.
```

### Tool 2: EditRichNote

**Description:**  
Edit a Mowen note supporting rich text formats, including **bold**, ==highlight==, [links](#), blockquotes, internal notes, images, audio, PDFs, and more.

**Prompt Example:**
```
Edit this note and expand the content to about 300 words.
```
```
Edit note iqP41aLx4V74zTlXE6Tqz, insert blank lines between paragraphs.
```

### Tool 3: ChangeNoteSettings

**Description:**  
Change note settings, such as making a note public or private.

**Prompt Example:**
```
Set this note to public.
```
```
Change note settings for iqP41aLx4V74zTlXE6Tqz, set to public.
```

### Tool 4: UploadViaURL

**Description:**  
Upload files via URL. Currently supports images, audio, and PDFs.

**Prompt Example:**
```
{URL} — save the image to Mowen.
```

## ScreenShot
<p align="center">
  <img src="https://pub-sdn-001.mowen.cn/mo/static/mcp/guide.png" style="width: 100%; height: auto;">
</p>

<p align="center">
  <img src="https://pub-sdn-001.mowen.cn/mo/static/mcp/sample.jpg" style="width: 100%; height: auto;">
</p>

## Supported Platforms

All AI IDEs and online tools that support the [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) protocol, such as Trae, Cursor, etc.

## Service Activation (Full Product)

1. Open the Mowen Mini Program (#小程序://墨问/ig4wUX5DvpMLRNJ)
2. Go to "My" at the bottom right
3. Activate "Mowen Membership"

## Authentication

After activating "Mowen Membership", go to the Developer Center to get your APIKey.

## Installation & Deployment

Mowen's MCP service is based on the [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) protocol, with no local environment dependencies. Any AI IDE or online tool that supports [Streamable HTTP](https://modelcontextprotocol.io/specification/2025-03-26/basic/transports#streamable-http) can be configured directly.

```
{
  "mcpServers": {
    "Mowen Assistant": {
      "url": "https://open.mowen.cn/api/open/mcp/v1/note?key=your-mowen-API-KEY"
    }
  }
}
``` 
