# clipper-templates

Templates that I use with [Obsidian Web Clipper](https://obsidian.md/clipper), inspired by [Kepano's own repo](https://github.com/kepano/clipper-templates).

I'm still slowly experimenting with my preferred layout so don't expect these to necessarily be stable.

## Kagi Summarizer

As part of clipping YouTube videos, I use Kagi's [Universal Summarizer API](https://help.kagi.com/kagi/api/summarizer.html) to include a takeaway summary of the video.

I do this by providing my own custom Provider in the Obsidian Clipper "Interpreter" tab:

Provider: Custom
Provider Name: Gunslinger
Base URL: https://gunslinger.utf9k.net/obsidian-web-clipper/kagi-summarizer?token=<snip>
API key: 123

This is followed by a custom model as well:

Provider: Gunslinger
Display name: Kagi Summarizer
Model ID: kagi-summarizer

When making a request, the interpret context, set as the video URL, is posted over to [Gunslinger](https://gunslinger.utf9k.net). This makes a call to the Kagi Universal Summarizer and returns the result in place of the `{{"kagi_summarizer_output"}}` block included in the "Note content" template.
