---
title: How to Insert Images into Anki Card
author: Victor Liang
categories: Anki
---





1. Copy the image File into the Folder collection.media

   <img src="/images/lu29099khvnzz_tmp_117f00af09f8357a.png" alt="img" style="width:600px;height:400px;" /> 

   

2. Add “field” IMAGE in your card. You can give the field with other names, of course.

   <img src="/images/lu29099khvnzz_tmp_bc8b9faa07f6b04e.png" alt="img" style="width:600px;height:400px;" /> 

   

3. Input image file name into the field IMAGE

   <img src="/images/lu29099khvnzz_tmp_bc8b9faa07f6b04e.png" alt="img" style="width:600px;height:400px;" /> 

   

4. Add the field in the template by typing:



   ```html
   {% raw %}
   <img src={{IMAGE}} />
   {% endraw %}
   ```

   

<img src="/images/lu29099khvnzz_tmp_d1758f36e75a78f.png" alt="img" style="width:h:400px;height:400px;" /> 

 

## Import from CSV file

If you need to import images into a deck by using CSV,

- Do steps 1-2

- Input the image file name in a column of CSV file

<img src="/images/lu29099khvnzz_tmp_fd4597a690f8a811.png" alt="img" style="width:600px;height:400px;" /> 

- Import the CSV into your deck, mapping the 3rd column IMAGE to the field you created in step 2

- Do step 4
