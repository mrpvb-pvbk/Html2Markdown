# HTML2Markdown
## mrpvb-pvbk mod with some advanced features

Converts HTML to [Markdown](http://daringfireball.net/projects/markdown/syntax).

---

![Html2Markdown](https://cloud.githubusercontent.com/assets/1049999/11505182/0480ad76-9841-11e5-8a62-126d4b7c03be.png)

## Support

This project will currently convert the following HTML tags:-

- `<a>`
- `<strong>`
- `<b>`
- `<em>`
- `<i>`
- `<br>`
- `<code>`
- `<h1>`
- `<h2>`
- `<h3>`
- `<h4>`
- `<h5>`
- `<h6>`
- `<blockquote>`
- `<img>`
- `<hr>`
- `<p>`
- `<pre>`
- `<ul>`
- `<ol>`

## Installing via NuGet base version

[![NuGet version](https://badge.fury.io/nu/Html2Markdown.svg)](http://badge.fury.io/nu/Html2Markdown)

```pwsh
    Install-Package Html2Markdown
```

## Usage

### Strings

```csharp
var html = "Something to <strong>convert</strong>";
var converter = new Converter();
var markdown = converter.Convert(html);
```

### Files

```csharp
var path = "file.html";
var converter = new Converter();
var markdown = converter.ConvertFile(path);
```

### Replace files in directory

```csharp
var dirPath = @"C:\Users\pvbk\Desktop\myhtmlfiles2replace\";
var converter = new Converter();
converter.ConvertFiles2Replace(dirPath);
```

## Customise

### Create new `IScheme` implementation

Create your own implementation of `IScheme` and construct `Converter` with that.

```csharp
var html = "Something to <strong>convert</strong>";
var converter = new Converter(customConversionScheme);
var markdown = converter.Convert(html);
```

## Try it

This library is showcased at [http://html2markdown.bayn.es](http://html2markdown.bayn.es).

## Contributing

[For those interested in contributing then please read the guidelines](CONTRIBUTING.md)

## License

This project is licensed under [Apache License 2.0](http://www.apache.org/licenses/LICENSE-2.0).