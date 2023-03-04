---
{"dg-publish":true,"permalink":"/10-wiki/random/"}
---

# Random
---
Here you can find a collection of 30 random notes from my wiki. This collection changes every week.

- [[10 Wiki/12 Notes/Capital Flow - 20230216083316\|Capital Flow - 20230216083316]]
- [[10 Wiki/12 Notes/Camarilla Pivot Point - 20230216083205\|Camarilla Pivot Point - 20230216083205]]
- [[10 Wiki/12 Notes/Breakout - 20230216071835\|Breakout - 20230216071835]]
- [[10 Wiki/12 Notes/Bloomberg Dollar Spot Index - 20230216070647\|Bloomberg Dollar Spot Index - 20230216070647]]
- [[10 Wiki/12 Notes/Bid - 20230215065026\|Bid - 20230215065026]]
- [[10 Wiki/12 Notes/Autosuggestion - 20230128053947\|Autosuggestion - 20230128053947]]
- [[10 Wiki/12 Notes/Availability Bias - 20230128054712\|Availability Bias - 20230128054712]]
- [[10 Wiki/12 Notes/Art Memory System - 20230127072040\|Art Memory System - 20230127072040]]
- [[10 Wiki/12 Notes/Bitcoin - 20230215071646\|Bitcoin - 20230215071646]]
- [[10 Wiki/12 Notes/Behavioral Patterns - 20230129065055\|Behavioral Patterns - 20230129065055]]
- [[10 Wiki/12 Notes/Builder - 20230216072034\|Builder - 20230216072034]]
- [[10 Wiki/12 Notes/Authority Principle - 20230128053542\|Authority Principle - 20230128053542]]
- [[10 Wiki/12 Notes/Behavioral Finance - 20230129064917\|Behavioral Finance - 20230129064917]]
- [[10 Wiki/12 Notes/ASFC - 20230127073205\|ASFC - 20230127073205]]
- [[10 Wiki/12 Notes/Adiabatic Cooling - 20230123112126\|Adiabatic Cooling - 20230123112126]]
- [[10 Wiki/12 Notes/Aerodynamic Resultant - 20230123022053\|Aerodynamic Resultant - 20230123022053]]
- [[10 Wiki/12 Notes/Aerodrome Integration - 20230123021122\|Aerodrome Integration - 20230123021122]]
- [[10 Wiki/12 Notes/Aeronautical Lubrification - 20230123105615\|Aeronautical Lubrification - 20230123105615]]
- [[10 Wiki/12 Notes/Aeronautical Train - 20230124103040\|Aeronautical Train - 20230124103040]]
- [[10 Wiki/12 Notes/Aileron - 20230124103842\|Aileron - 20230124103842]]
- [[10 Wiki/12 Notes/Airbrakes - 20230125033043\|Airbrakes - 20230125033043]]
- [[10 Wiki/12 Notes/Ammeter - 20230126110013\|Ammeter - 20230126110013]]
- [[10 Wiki/12 Notes/Anemometer - 20230126110635\|Anemometer - 20230126110635]]
- [[10 Wiki/12 Notes/Angles of the Aircraft - 20230126112051\|Angles of the Aircraft - 20230126112051]]
- [[10 Wiki/12 Notes/Autan - 20230128054212\|Autan - 20230128054212]]
- [[10 Wiki/12 Notes/Ball - 20230215070009\|Ball - 20230215070009]]
- [[10 Wiki/12 Notes/Barotrauma - 20230129063239\|Barotrauma - 20230129063239]]
- [[10 Wiki/12 Notes/Carburettor Icing - 20230216083857\|Carburettor Icing - 20230216083857]]
- [[10 Wiki/12 Notes/Ground to Air Signals - 20230123012741\|Ground to Air Signals - 20230123012741]]
- [[10 Wiki/12 Notes/Bias Variance Tradeoff - 20230215064841\|Bias Variance Tradeoff - 20230215064841]]


## How is this Done?
I do this automatically with the following Python script:

```python
"""  
This script will add a tag to a random subset of notes in a folder.  
"""  
  
  
import os  
import re  
import random  
import yaml  
  
folder_path = r"/path/to/your/notes/folder"
n = 30  # number of random notes to tag  
random_tag_name = "wiki/meta/random"  # name of the tag to add  
  
files = os.listdir(folder_path)  
random_files = random.sample(files, n)  
  
for filename in files:  
    with open(os.path.join(folder_path, filename), 'r', encoding='utf-8') as file:  
        file_content = file.read()  
  
        frontmatter = re.findall(r'---\n(.*?)\n---', file_content, re.MULTILINE | re.DOTALL)  
        if frontmatter:  
            frontmatter = frontmatter[0]  # get the first match (there should only be one)  
            frontmatter = yaml.safe_load(frontmatter)  
  
        tags = frontmatter.get("tags", []) or []  
        if isinstance(tags, str):  
            tags = tags.split(",")  # because I usually use a comma-separated string instead of a list  
        if random_tag_name in tags:  
            tags.remove(random_tag_name)  
  
        if filename in random_files:  
            print(f"Adding {random_tag_name} to {filename}...")  
            tags.append(random_tag_name)  
  
        tags = [tag.strip() for tag in tags]  
  
        frontmatter["tags"] = tags  
        file_content = re.sub(r'---\n(.*?)\n---', f'---\n{yaml.dump(frontmatter)}---', file_content, 1, re.MULTILINE | re.DOTALL)  
  
        with open(os.path.join(folder_path, filename), 'w', encoding='utf-8') as file:  
            file.write(file_content)
```