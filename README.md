#t.me/kt7kt
from tqdm import tqdm
import instaloader,pyperclip , pyfiglet ,os ,webbrowser,random,time
A = "\033[1;91m" #احمر
B = "\033[1;90m" #رمادي
C = "\033[1;97m" #ابيض
E = "\033[1;92m" #اخضر
H = "\033[1;93m" #اصفر
K = "\033[1;94m" #بنفسجي
L = "\033[1;95m" #بنفسجي
M = "\033[1;94m" #ازرق
R = '\033[31;1m' #احمر
print ('\033[1;93m')
font = pyfiglet.figlet_format("Explore Tool", font="slant")
print(font)
webbrowser.open ("tg://join?invite=SzaNtj51XvgKvTuF")
print ("\033[1;97m------------------------")
username = input("Enter The username:")
L = instaloader.Instaloader()
def get_random_user_agent():
    os_platforms = ['Windows NT 10.0; Win64; x64', 'Windows NT 6.1; Win64; x64', 'Macintosh; Intel Mac OS X 10_15_0', 'Linux x86_64']
    browsers = ['Chrome', 'Firefox', 'Safari', 'Edge']
    user_agent = f"{random.choice(browsers)}/{random.randint(1, 100)}.{random.randint(0, 100)} ({random.choice(os_platforms)})"
    return user_agent

profile = instaloader.Profile.from_username(L.context, username)
num_copies = int(input("\033[1;93m●\033[1;92m Enter number copy link: "))
print ('\033[1;93m')
for i in tqdm(range(num_copies), desc="Copying Latest Link"):
    time.sleep(2)
    L.context.headers = {'User-Agent': get_random_user_agent()}
    latest_post = None
    for post in profile.get_posts():
        latest_post = post
        break
    if latest_post:
        latest_post_shortcode = latest_post.shortcode
        latest_post_url = f"https://www.instagram.com/p/{latest_post_shortcode}/"
        pyperclip.copy(latest_post_url)
    else:
        print("No posts found")
print ("Like And Follow me")
time.sleep(0.5)
other_username = "rb98"
other_profile = instaloader.Profile.from_username(L.context, other_username)
latest_post = None
for post in other_profile.get_posts():
    latest_post = post
    break
if latest_post:
    latest_post_shortcode = latest_post.shortcode
    latest_post_url = f"https://www.instagram.com/p/{latest_post_shortcode}/"
    webbrowser.open(latest_post_url)
else:
    print("No posts found for this user")
