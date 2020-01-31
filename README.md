# pdfwatermark
Watermark PDF documents

pdfwatermark is a simple, yet effective tool to watermark your personal
documents before handing them to some people/corporation.

While it might be sufficient for most people at most time in life, the increased
security provided by this software is absolutely not bullet-proof, nor even
guaranted. Use at your own risks.

## Usage

```
Usage: pdfwatermark [OPTION]... <WATERMARK> <FILE>...
Watermark your PDF documents

Mandatory arguments to long options are mandatory for short options too.
  -d, --directory DIR       set DIR instead of /tmp/pdfwatermark.<mktemp> as
                              working directory (implies --keep-files)
  -D, --force-dir DIR       as -d, but force creation of DIR if is doesn't exist
  -f, --force               do not ask for overwrite confirmation
  -k, --keep-files          keep intermediate files instead of deleting them
      --opacity N           set watermark inclusion opacity to N (0-100)
  -v, --verbose             be verbose
  --help                    display this help and exit

Full documentation <https://www.github.com/bacara/pdfwatermark>
```

## How to create your watermark

### Using GIMP

At startup, choose File > New. In the popup window, choose the A4 template. Enable
advanced options, then set "Fill Background" to "Transparency". Create the new file.

Now, you can just use the text tool to make your watermark. Use a dark color, if
not black for your text and use pdfwatermark --opacity option to fine tune
afterwards. Remember this is an A4 sized image: you might want to increase
default text size. Once you're done, export the file to PNG.

## Troubleshooting and known issues

### My watermark is not visible in the document

Using this tool, one missue that might occur is that you don't see the watermark
in the file. This happens when the original PDF is not having the same ppi as
the watermark (GIMP default is 300 ppi). If this is your case, try using a
smaller part of your watermark template to make it fit inside your document. The
author is aware this is a crappy workaround, but do not have any better solution
at the moment. If you think you do have an idea or some chunks of code to
enhance this solution, please contribute.
