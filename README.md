# Developer Assessment

## Expected Outcome

#### 1. Explain how would you test this component using Unit testing and Snapshot testing (and how you would address accessibility).

To test this component using Unit testing I could write a separate test for each section of the component that checks that it's showing up as expected, or I could write one test to verify the entire thing is working correctly. I would use Jest or Jasmine to run the tests.

To test this component using Snapshot testing I would check that each image loads and displays properly, as well as verifying that all text shows up correctly and is readable by screen readers. I would use Jest or Jasmine to run the snapshot tests.

To ensure accessibility, I would use tools like [accessiBe](https://accessibe.com/) or Color Ratio Rating from Chrome Dev Tools or similar tools to check my code for any issues.

#### 2. Explain how you would deploy using CI/CD pipeline (considering the testing phase as well) and hosting in an Amazon S3 bucket.

That depends on the resources I have available. 
1. To automate the deployment process, I would use AWS CodePipeline. That is the process that allows me to push code to a specific branch of the repository, and then automatically deploy that branch to a specific environment. Then I would use AWS CodeDeploy to deploy the code to the staging environment. Finally I would merge the staging environment into the master branch and deploy that to the production environment. Or
2. A more "manual" process woule be to push the code to a dev branch, build the source code, run the test, and then merge and deploy to staging branch and env. Then I would merge the staging into the master branch and deploy to production. To automate the process I would use GitHub Actions.

#### 3. Explain things that could go wrong with this component design / code

There are a few things that could go wrong with this component.
First is that the component design as shown on the doc is not responsive. I would have to make sure that the component is responsive on mobile and desktop and that requires cross-browser testing to ensure that it works as expected on all devices and browsers.
Second, the instances of this component could not be unique. This means that if we have more than one instance on a page, they could all update at once, which may not be what we want.
Finally, Vanilla JS is not supported on all browsers till this day or some users have it disabled. I need to make sure that it works on as many browsers as possible so that users with older browsers can still see and use this component without issue.

#### 4. If you would use a framework (React, Vue JS, Angular) to build this component what could be improved?

If I were to use a framework, I would first look at what the framework does for me. What does it do for me that I don't have to worry about.

1. If I'm using React, then all of my "HTML" will already be in one file. It's easy to see which components are being called and where they're being used. It also makes sure that all of the CSS rules are going to the right place—and that they match up with their elements. Or
2. If I were building this component with Vue JS, then there would also be some nice features built into it (such as being able to use a template engine like Pug). These are things that I might not want to build by hand because they're very specific to this particular use case, but if they exist within Vue JS, then why not take advantage of them.

> **Note:** As you mentioning on the tasks in the doc, I only used HTML5, CSS3 and Vanilla JS. I didn't use any frameworks as that wasn't mentioned in the doc. Also I wasn't sure how you wanted me to use Vanilla JS in this case, as it wasn't any obvious way shown on the design, so I just used it as a way to generate the data in the DOM.

**Thank you this opportunity!**