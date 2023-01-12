# Unfollow Everything On Facebook
It is a script to unfollow everything on Facebook

1. Open https://www.facebook.com/pages/?category=liked
2. Scroll down to load all pages
3. Open Developers Tools in your browser on a PC (CTRL+ALT+I or search online <browser name> + open developer tools). The following tutorial is based on Chrome unfortunately
4. Open a place to paste the script to unfollow. Go to "Sources" tab
5. Click "New snippet"
6. In the text field paste:

```
var xpath = "//span[text()='Obserwujesz']";
var matchingElement = document.evaluate(xpath, document, null, XPathResult.ORDERED_NODE_SNAPSHOT_TYPE, null);
for (var i = 0; i < matchingElement.snapshotLength; i++)
{
  matchingElement.snapshotItem(i).click();
}
```

'Obserwujesz" is the text displayed on the button below a fanpage on the list:
  
![image](https://user-images.githubusercontent.com/834977/212021379-84575569-c35a-4600-a0f2-6f12babb38f9.png)

In case you don't use polish language, change it to the text you see on the button.
Some people run the script with 'Following' and 'Liked' texts to wipe all likes and follows.

7. Click CTRL+ENTER or the arrow below to run the script
8. The script will unfullow / unobserve all fanpages. Now you can enjoy Facebook without spam

Facebook is a trademark of Facebook

# Troubleshooting

If it does not work, create an issue with a screenshot of your page
