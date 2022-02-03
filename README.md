# Reading-presentation-pptx-file
Using Python to read a presentation (pptx) file and get its text
# install python-pptx
pip install python-pptx

# install glob
pip install glob

# import glob library
import glob

# import presentation from glob
from pptx import Presentation

# fpr loop to read each slide in the pptx
for eachfile in glob.glob("*.pptx"):
  # choose the file we want to read
  prs = Presentation("Test.pptx")
  # to read slides one by one
  for slide in prs.slides:
    # read the text in each slide
    for shape in slide.shapes:
      # if condition to check if this is a text or not
      if hasattr(shape, "text"):
        text=shape.text
        # print the text
        print(text)
    # take line after each slide in the file
    print("....................")
