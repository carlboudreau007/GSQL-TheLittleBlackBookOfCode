# GSQL - The Little Black Book Of Code
This is a collection of Tips &amp; Trick and How-Too's to write and overcome difficult challenges with in TigerGrap and the GSQL language.

# Using Default Parameters
This is a collection of GSQL statements show how to use default parmeters in a GSQL query

        CREATE QUERY defaultParms(INT age = 3, STRING name = "John",
            DATETIME birthday = to_datetime("2019-02-19 19:19:19"))
        {
          PRINT age, name, birthday;
        }

Use underscores (_) to indicate the use of the default parmeter.

Like;
        RUN QUERY defaultParms (21, _, "2020-02-02 20:02:20")

This repository is will always be work in progress.  I will try to sort the folder structure thinking ahead but I will never be smarter today than I will be tomorrow.  So please bear with me.

[FOLDER NAME HERE]
[Descritopn of contents here]

If you have questions, comments or would like to contribute please let me know

Carl Boudreau | carl.boudreau@tigergraph.com | carlboudreau007@gmail.com | https://www.linkedin.com/in/graphy-giraffe/
