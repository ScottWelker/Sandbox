# Add an image
This was surprisingly troublesome. No doubt due to my refusal to use full-blown URLs that I'd have to first figure out. Wiki needs to be quick and easy. Futzing with these URLs, as the documentation directs, does not seem quick and easy. 

- [Embedding images inside a GitHub wiki (gollum) repository?](https://stackoverflow.com/questions/10045517/embedding-images-inside-a-github-wiki-gollum-repository) gave me the ideas yielding the following, mostly-working, solution.

I had success as follows but it's apparently non-standard.
1. Cloning the Wiki's underlying repository.
1. Adding an `images` folder to which I added my `programming.png` image.
1. Adding, committing, and pushing the changes back to "_origin_."
1. Editing the page and adding the `![An Image](images/programming.png)` below.
   - **WARNING** The image does not display within the page editor's `Preview` tab. Had to save the page and view it '_normally_' to see the image. 
      - Strangely, adding ` ![An Image](../images/programming.png)` instead has the reverse result, i.e. I was then able to preview the image but it did not render correctly in the saved page. 

- ![An Image](.attachments/programming.png)