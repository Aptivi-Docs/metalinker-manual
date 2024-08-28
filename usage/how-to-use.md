---
description: How do I use this library?
icon: computer
---

# How to use

You can easily parse both Metalink 3.0 and 4.0 files, streams, and XML representations by using the following functions that are available in the `MetalinkParser` class:

* `GetMetalinkFromPath(string file)`
  * This function parses the Metalink data by giving it a file path
* `GetMetalinkFromStream(Stream stream)`
  * This function parses the Metalink data by giving it a stream
* `GetMetalinkFromXml(string metalink)`
  * This function parses the Metalink data by giving it an XML representation
* `GetMetalinkFromXmlDocument(XmlDocument metalinkDocument)`
  * This function parses the Metalink data by giving it an XML document instance that contains an XML representation of a Metalink data

This is very easy; just call one of these functions when assigning a variable that will hold Metalink-related data, and you'll be able to get information about the file, such as hashes, chunks and their info, and regions for mirrors. Here's a very simple example of how to do this using a file stream:

```csharp
// Note that MetalinkLoader is not part of the library
Stream? stream = MetalinkLoader.LoadMetalinkStream("slackware15.iso.metalink");
if (stream is null)
    Assert.Fail("Stream is null");
 var metalink = MetalinkParser.GetMetalinkFromStream(stream);
```
