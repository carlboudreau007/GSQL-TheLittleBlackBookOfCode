# GSQL - The Little Black Book Of Code

With the  data in below example:
id, latitude, longitude
1,"latitude=40.75","longitude=-73.97"
2,"latitude=53.35","longitude=-6.21"
3,"latitude=40.75","longitude=-73.97"
4,"latitude=45.54","longitude=-122.83"

I need to extract the float value and ingest it as FLOAT;

CREATE LOADING JOB load_job_gps FOR GRAPH myGraph {
    DEFINE FILENAME gps_data;
    LOAD gps_data TO VERTEX locations VALUES(
        $0,
        gsql_str_to_float(gsql_trim(gsql_regex_replace($27,"^[^=]+=",""))),
        gsql_str_to_float(gsql_trim(gsql_regex_replace($28,"^[^=]+=","")))
    ) USING SEPARATOR=",", HEADER="true", EOL="\n", QUOTE="double";
}

If you have questions, comments or would like to contribute please let me know

Carl Boudreau | carl.boudreau@tigergraph.com | carlboudreau007@gmail.com | https://www.linkedin.com/in/graphy-giraffe/
