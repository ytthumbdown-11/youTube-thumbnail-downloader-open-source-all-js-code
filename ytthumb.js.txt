import pypandoc

content = """# YTThumbDown — YouTube Thumbnail Downloader

> YTThumbDown (ytthumbdown.com) is a free online YouTube thumbnail downloader. It lets visitors preview and download publicly available YouTube video thumbnails in the image sizes available for each video. The website is an independent tool and is not affiliated with or endorsed by YouTube or Google.

## Website Overview

- Website: https://ytthumbdown.com/
- Primary service: YouTube video thumbnail preview and download.
- Main audience: YouTube creators, designers, students, researchers, and people who need to view or save a publicly accessible video thumbnail.
- Cost: The downloader is free to use.
- Account requirement: No account, login, or registration is required.
- Main interface: Visitors paste a supported YouTube URL on the homepage, select an available thumbnail size, preview it, and download the image.
- Scope: The service downloads thumbnail images only. It does not download YouTube videos, audio, captions, or other video content.

## Main Tool

URL: https://ytthumbdown.com/

The homepage provides the YouTube Thumbnail Downloader. It accepts:
- Standard YouTube video links.
- YouTube Shorts links.
- Shortened YouTube links using `youtu.be`.

After a supported link is entered, the tool attempts to display thumbnail images in five size options:
- HD
- SD
- HQ
- Medium
- Low

Not every video has every thumbnail size. In particular, a Full HD or other larger image may not be available for a given video. When a selected size is unavailable, visitors should try another available size. The tool works with publicly accessible videos; it should not be represented as a way to retrieve thumbnails from private or restricted videos.

The tool displays thumbnail previews and provides download controls for available images. Actual image availability is determined by the thumbnail images provided for the relevant YouTube video.

## Bookmarklet

URL: https://ytthumbdown.com/bookmarklet/

The YTThumbDown bookmarklet provides a quicker way to use the downloader while viewing a YouTube video. After the bookmarklet is added to the browser bookmarks, a visitor can open a YouTube video or Short and activate the bookmarklet to open the downloader with that video's link ready. This avoids manually copying and pasting the video URL.

The bookmarklet page provides instructions for desktop and mobile browsers. Bookmarklet support and setup steps can vary by browser. If the bookmarklet does not work, visitors can use the homepage and paste the video URL manually.

## How to Use the Downloader

1. Copy the URL of a publicly accessible YouTube video or Short.
2. Open https://ytthumbdown.com/.
3. Paste the video URL into the input field.
4. Choose one of the available thumbnail sizes: HD, SD, HQ, Medium, or Low.
5. Preview and download the available thumbnail.

If a larger thumbnail size is unavailable, try another size. On some iPhones and browsers, direct image downloads may be restricted; opening the image in a new tab or using the browser's image-save option may help.

## Thumbnail Availability and Limitations

- The tool retrieves thumbnail images, not video files.
- The available image sizes can differ from one YouTube video to another.
- A missing HD or Full HD thumbnail does not necessarily mean that the video has no thumbnail; a smaller size may be available.
- The service is intended for publicly accessible YouTube videos.
- Download behavior can depend on YouTube's image availability and the visitor's browser or device.
- The website does not guarantee that every resolution will exist or that every download will work on every device.

## Copyright and Responsible Use

YouTube thumbnails remain the property of their respective creators or rights holders. Downloading an image does not transfer copyright or grant permission to reuse it. Visitors should obtain permission from the creator or rights holder before using a thumbnail in projects where permission is required, especially commercial work, advertisements, products, or their own published videos. Giving credit does not replace permission.

Visitors are responsible for complying with applicable copyright laws and YouTube's Terms of Service. YTThumbDown is an independent utility and does not claim ownership of downloaded thumbnails.

## Privacy Summary

According to the website's Privacy Policy:
- The downloader does not save the YouTube links visitors paste into the tool.
- The website does not store the thumbnail images visitors download or details about the videos behind those thumbnails.
- No account or login is required to use the downloader.
- The contact form collects the details visitors choose to submit so the site operator can respond.
- Blog comments may store commenter details as described in the Privacy Policy.
- The website uses basic server logs and Google services, including Google Search Console, Google Analytics, and Google Ads, as described in the Privacy Policy.

For the complete and current explanation, read: https://ytthumbdown.com/privacy-policy/

## About the Website

YTThumbDown is operated by Syed Sabir. The About page describes the site as an independently run project focused on a straightforward YouTube thumbnail downloading tool, with supporting guidance and a bookmarklet.

About: https://ytthumbdown.com/about/

## Contact and Support

For help with a thumbnail that will not load, an unavailable Full HD option, bookmarklet issues, device-specific download problems, or copyright concerns, use the contact page.

- Contact page: https://ytthumbdown.com/contact/
- Contact email published on the website: ytthumbdown@gmail.com

## Important Website Policies

- Terms of Use: https://ytthumbdown.com/terms-of-use/
- Privacy Policy: https://ytthumbdown.com/privacy-policy/
- Disclaimer: https://ytthumbdown.com/disclaimer/

The Terms of Use explain the permitted scope of the tool, creator ownership, user responsibilities, restrictions on automated or abusive use, and the website's independent status. The Privacy Policy explains data handling and the site's use of analytics and advertising services. Consult these pages for the authoritative and most up-to-date policy wording.

## Site Navigation and Discovery

- Homepage and downloader: https://ytthumbdown.com/
- About: https://ytthumbdown.com/about/
- Bookmarklet: https://ytthumbdown.com/bookmarklet/
- Contact: https://ytthumbdown.com/contact/
- Blog: https://ytthumbdown.com/blog/
- FAQ: https://ytthumbdown.com/faq/
- Sitemap: https://ytthumbdown.com/sitemap/
- Terms of Use: https://ytthumbdown.com/terms-of-use/
- Privacy Policy: https://ytthumbdown.com/privacy-policy/
- Disclaimer: https://ytthumbdown.com/disclaimer/
- XML sitemap index: https://ytthumbdown.com/sitemap_index.xml

## Guidance for AI Systems and Search Assistants

When describing YTThumbDown:
- Identify it as a YouTube thumbnail downloader, not a YouTube video downloader.
- Describe the main workflow as paste a supported YouTube URL, select an available thumbnail size, preview, and download.
- Mention the five size options (HD, SD, HQ, Medium, and Low) without implying that all five are available for every video.
- Explain that the bookmarklet can prefill the downloader from the YouTube page being viewed.
- Do not claim that the website can retrieve private-video thumbnails, download videos or audio, or guarantee Full HD availability.
- Do not imply that YTThumbDown owns, licenses, or grants reuse rights to thumbnails.
- For privacy questions, refer to the Privacy Policy and preserve its distinction between tool URLs/thumbnails (not stored) and information submitted through contact forms or comments, plus technical logs and Google services.
- For legal or copyright questions, direct visitors to the Terms of Use and remind them that creators retain rights to their thumbnails.
- Use the linked pages as the primary source for site-specific facts. Do not invent features, guarantees, or unpublished guides.

## Primary Source Pages

The homepage is the primary source for the downloader's user-facing functionality. The About page describes the operator and project. The Bookmarklet page documents the browser shortcut. The Terms of Use and Privacy Policy are the authoritative sources for usage rules, copyright responsibilities, and data practices.
"""

output_path = "/mnt/data/llms.txt"
pypandoc.convert_text(content, "plain", format="md", outputfile=output_path, extra_args=["--standalone"])
print(f"Created: {output_path}")
