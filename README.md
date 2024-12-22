# Crawl-LIB---With-libcurl-and-c-
A Simple Lightweight C++ Library For Crawling Webpages

Start Writting your code with this docs!

## Installing
You will need libcurl to be installed first and then you may run the following command
```bash
git clone https://github.com/ghgltggamers/Crawl-LIB---With-libcurl-and-c-.git
mv Crawl-LIB---With-libcurl-and-c-/crawl.hpp .
rm -rf Crawl-LIB---With-libcurl-and-c-
echo "Installed!"
echo ""
```

# API Reference
Methods
# fetchWebpage(const std::string& url)

Fetches the HTML content of the specified URL.

    Parameters:
        url: The URL of the webpage to fetch.
    Returns:
        A std::string containing the HTML content.
    Throws:
        std::runtime_error if the request fails.

# extractLinks(const std::string& webpageContent)

Extracts all hyperlinks from the provided HTML content.

    Parameters:
        webpageContent: The HTML content as a string.
    Returns:
        A std::vector<std::string> containing all the hyperlinks.

# isCrawlingAllowed(const std::string& url)

Checks if crawling is allowed for the specified URL by parsing its robots.txt file.

    Parameters:
        url: The URL to check.
    Returns:
        true if crawling is allowed.
        false otherwise.

Helper Functions

    Write Callback: Handles data from curl and appends it to a string.
    Domain Extraction: Extracts the domain from a URL for robots.txt checks.
    robots.txt Parsing: Ensures the crawler respects disallow rules.

Notes

    If robots.txt is not accessible, the crawler assumes crawling is allowed.
    The class currently supports only basic link extraction using regex. More robust parsing may require an HTML parser library.

License

This implementation is open-source and available under the MIT License.
