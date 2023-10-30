class Trent:
    def __init__(self, name, age, interests, browser, operating_system, socials):
        self.name = name
        self.age = age
        self.interests = interests
        self.browser = browser
        self.operating_system = operating_system
        self.socials = socials

    def generate_bio(self):
        bio = "Name: {}\n".format(self.name)
        bio += "Age: {}\n".format(self.age)
        bio += "Interests: {}\n".format(", ".join(self.interests))
        bio += "Browser: {}\n".format(self.browser)
        bio += "Operating System: {}\n".format(self.operating_system)
        bio += "Socials: \n"
        for platform, username in self.socials.items():
            bio += "{}: {}\n".format(platform.capitalize(), username)
        return bio

# Define Information
name = "Trent"
age = 15
interests = ["Gaming", "Computers", "Keyboard", "Mice"]
browser = "Chrome"
operating_system = "Windows"
socials = {
    "Email": "m3nnis0@gmail.com",
    "Discord": "https://discord.gg/x8xnhbpYFt"
}

# Create bio
trent = Trent(name, age, interests, browser, operating_system, socials)
bio = trent.generate_bio()
print(bio)
