from selenium import webdriver
from selenium.webdriver.common.by import By
import time

# 1. Setup the browser (Chrome)
driver = webdriver.Chrome() 

def watch_video(url):
    # 2. Open the TikTok video
    driver.get(url)
    print("Video opened. Watching for 20 seconds...")
    
    # 3. Wait (simulates watching the video)
    time.sleep(20) 
    
    # 4. Find and click the 'Like' button (Example selector)
    try:
        like_button = driver.find_element(By.XPATH, '//span[@data-e2e="like-icon"]')
        like_button.click()
        print("Liked the video!")
    except:
        print("Could not find the like button (it might be hidden or the page changed).")

# Run the function
watch_video("https://www.tiktok.com/@username/video/123456789")

# Keep the window open for a bit then close
time.sleep(5)
driver.quit
