# Protocol Primer

Protocol Primer is a website dedicated to explaining technical changes in Bitcoin in simple, neutral language.

## About

This repository hosts the Protocol Primer website, built with Jekyll and the Minimal Mistakes theme. The site is deployed using GitHub Pages.

## Local Development

To run this site locally:

1. Install Ruby and Bundler
2. Clone this repository:
   ```
   git clone https://github.com/Talks2Bots/protocolprimer.git
   cd protocolprimer
   ```
3. Install dependencies:
   ```
   bundle install
   ```
4. Start the local server:
   ```
   bundle exec jekyll serve
   ```
5. Visit `http://localhost:4000` in your browser

## Adding Content

### Creating a new post

1. Add a new Markdown file in the `_posts` directory following the naming format `YYYY-MM-DD-title.md`
2. Include the proper front matter at the top of the file:
   ```
   ---
   title: "Your Post Title"
   date: YYYY-MM-DD
   categories:
     - Category
   tags:
     - tag1
     - tag2
   ---
   ```
3. Write your content using Markdown

## License

This project is available as open source under the terms of the [MIT License](LICENSE). 