# Blog Requirements

In this document, I will describe what the core requirements will be for the `Blog` feature that I am developing and demonstrating on my YouTube channel.

## Core Features

1. There should be an article that includes the following information
    * Title, Summary, BodyText, Category Taxonomy, Tagging Taxonomy, Author Information, A thumbnail for the listing pages on the site, and related articles.
2. You should be able to leave a comment on an article, that comment should include the following information:
    * Name, Email, BodyText
3. Information entered into the comment for should be added to xDb based on the submission.  This should also have the ability to add to a goal or engagement plan.
3. You should be able to Share the current article to social channels and that information should be tracked within Sitecore.
4. There will be an Archive page, on this page, it will handle the following:
    * Facet based on the Category and Author
    * Sort by Most Recent, Most Relevant (when performing a search) or alphabetical (default).
    * The page should only show 12 by default, but the editor should be able to change this value quickly.  After showing 12 listings it should paginate.
    * The archive page should also allow for a Querystring/or context item by "Category" to display only that category.
    * The archive page should also allow for a Querystring/or context item by "Author" to display only that author.
    * The Title, Summary and thumbnail should be displayed on this page.
5. The blog landing page should include the # most recent articles, which can be personalized as needed to show varied results.
6. Add the ability to have a `Featured` Article, which there will be multiple placements for this on the homepage and various other pages.
7. Create a Related articles component, this will pull # listings, this component should allow for personalization.
8. A category will consist of a Title and Summary Field.
9. Create a form that takes the users name and email, so they will be notified of upcoming blog posts. This will add them to predefined lists in (Provider).
    * Add data to xDb using xConnect
    * Add user to marketing automation plan
    * Add ability to trigger a goal
10. An Author will consist of a Name, Biography, Collection of Links, and a thumbnail of that author.



## Marketing Objectives

In addition to the development goals, we are going to want to achieve various goals with the marketing customization and data collected to drive better goals.  We want to achieve the following outcomes:

1. Increase Subscriptions/Newsletter Signups
2. Increase Social Metrics (Re-shares and Likes)



### Personas

1. The Enthusiast
    * 
2. The Researcher
3. 