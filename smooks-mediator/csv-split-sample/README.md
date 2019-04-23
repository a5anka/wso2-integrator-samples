# Using Smooks mediator to transform a large CSV file to XML

## Running the sample

1. Copy required configurations to EI_HOME.
    ```
    $ cp -r wso2ei-6.4.0/* $EI_HOME
    ```

2. Start Integrator profile.
   ```
   $ $EI_HOME/bin/integrator.sh
   ```

3. Build Carbon application with the synapse artifacts.
    ```
    $ cd smooks-csv-to-xml
    $ mvn clean install
    ```

4. Copy the created carbon application to EI deployment directory.
    ```
    $ cp smooks-csv-to-xml-capp/target/smooks-csv-to-xml-capp_1.0.0.car $EI_HOME/repository/deployment/server/carbonapps/
    ```

5. Create data directories and copy input data.
    ```
    # Go back to the sample home
    $ cd ..
    $ mkdir -p /tmp/smooks-sample/csv/in
    $ cp data/data.csv /tmp/smooks-sample/csv/in/
    ```

6. Check output in `/tmp/smooks-sample/csv/output/`
