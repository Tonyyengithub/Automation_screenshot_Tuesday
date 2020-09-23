# Automation_scrrenshot
Mission: Saving operator click time and switch cost, saving estimated five hours per week.
Result: Keep renewing the the photos in the folder until the procedure ended.

We utilize chromedriver to micmic the behavior of the click.

<img src = "https://github.com/Tonyyengithub/Automation_scrrenshot_Tuesday/blob/master/demo/photo.jpg" width = "600">

expanding the hiding pages in the webpage
```
driver.find_element_by_xpath('//*[@id=\"app\"]/div[2]/div[4]/div[2]/div').click()
```

Finding the target URL and apped it into a list, we need to remove the unrelated URL in this steo by 'pop' or 'remove'.
```
soup = BeautifulSoup(content.text, "html.parser") # finding all the page we want to reach
webs = []
for k in soup.find_all('a'):
    web = 'https://buy.line.me' + k['href'] # the URL is placed after href
    webs.append(web)
```

Scratching the product name in order to name the photo with their name.
```
soup = BeautifulSoup(content.text, "html.parser")
soup_list = soup.findAll('div', class_ = "card-productName") # profuct name is placed in 'card-productName' class
```



Result:
The bottom right folder will keep renewing the photo in the webpages

<img src = "https://github.com/Tonyyengithub/Automation_scrrenshot_Tuesday/blob/master/demo/demo.png" width = "1200">

