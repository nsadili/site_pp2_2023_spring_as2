<h1> Assignment 2 </h1>
<h3> Creating a simple JAVA application to implement File I/O and Filtration </h3>

Dear students,

In this assignment, you need to submit you work to implement File I/O and Filtration (we have partially completed
similar tasks during the
classes).

<h3>Task Related - List of the required types</h3>
<ul>
    <li>Country class</li>
</ul>

<h3>Task Related - Country class <strong>(20 %)</strong></h3>
<p>It should have the following fields and the methods:</p>
<p>Fields:</p>
<ul>
    <li><strong><em>id</em></strong> - (String)</li>
    <li><strong><em>countryName</em></strong> - (String)</li>
    <li><strong><em>continent</em></strong> - (String)</li>
    <li><strong><em>popultion</em></strong> - (Double - represented in thousand dollars)</li>
    <li><strong><em>IMF_GDP</em></strong> - (Double - represented in scientific notation)</li>
    <li><strong><em>UN_GDP</em></strong> - (Double - represented in scientific notation)</li>
    <li><strong><em>IMF_GDP_per_capita</em></strong> - (Double - represented in scientific notation)</li>
    <li><strong><em>UN_GDP_per_capita</em></strong> - (Double - represented in scientific notation - Missing in the data
        source)</li>
</ul>
<p>Methods:</p>
<ul>
    <li>necessary constructor(s)</li>
    <li>a getter method for each field</li>
    <li><strong><em>static parseFrom(String countryRecord) : Country</em></strong> - parses the given string
        (comma-separated) to create an instance of Country and returns it</li>
    <li><strong><em>parseTo() : String</em></strong> - parses the current country instance to a string record
        (comma-separated) to be later stored in a file</li>
    <li><strong><em>static parseTo(Country countryInstance) : String</em></strong> - parses the given country instance
        to a string record (comma-separated) to be later stored in a file. Hint: You may use already defined instance
        method to delegate the job</li>
    <li>Note: in the instatiation of a Country, if possible calculate and set the <strong>UN_GDP_per_capita</strong>
    </li>
</ul>

<h3>Task Related - FileManager class <strong>(20 %)</strong></h3>
<p>It should have the following fields and the methods:</p>
<p>Fields:</p>
<ul>
    <li><strong><em>static final COUNTRIES</em></strong> - (List)</li>
</ul>
<p>Methods:</p>
<ul>
    <li><strong><em>static loadCountries()</em></strong> - returns a list of countries reading the original data source
    </li>
    <li><strong><em>static saveCountries(List<Country> countries, String fileName)</em></strong> - generates a file with
        the given filename (under the data folder) and stores the list of countries in the file. (You may or may not include column names or
        header in the file)</li>
    <li>Any additional methods that would help you complete the task can be added</li>
</ul>

<h3>Task Related - Exception handling <strong>(10 %)</strong></h3>
<ul>
    <li>Please, carefully follow the instructions above.</li>
    <li>Your program should properly enforce encapsulation, file i/o, collections, and streams</li>
    <li>Your program should prevent invalid operations using proper exceptions and exception handling. Some of them are
        the following:
        <ul>
            <li>specified file is not found</li>
            <li>given string cannot be parsed to a country</li>
            <li>attempt to overwrite an existing file</li>
            <li>etc.</li>
        </ul>
    </li>
</ul>

<h3>Task Related - Testing all together <strong>(50 %)</strong></h3>
You will need to define a <strong><em>GDPDemo</em></strong> class which demonstrates all the functionality of
your program. However, it is strongly encouraged to test each class and each method as soon as they are completed to
have
less errors and easy debugging in the end. <br />
When you compile, make sure your .class files are totally isolated from the rest and are <strong>never commited and
    pushed</strong>.
<h4>Queries (to be executed in GDPDemo):</h4>
<ul>
    <li>Load all the countries from <i>countries.csv</i></li>
    <li>
        Sorting:
        <ul>
            <li><strong>(10 %)</strong>Define a method sort(List<Country> countries, String fieldName, String order)
                    method to sort the list of
                    all countries based on the given field and order</li>
            <li>Call the sort method to sort all countries based on the continent (first) and country names</li>
            <li>Save the result in a .csv file (name the file as descriptive as possible)<strong>(5 %)</strong></li>
            <li>Call the sort method again to sort all countries based on the descending order of population</li>
            <li>Save the result in a .csv file (name the file as descriptive as possible)<strong>(5 %)</strong></li>
        </ul>
    </li>
    <li>
        Filtration:
        <ul>
            <li><strong>(10 %)</strong>Define a method filterByContinent(List<Country> countries, String continent)
                    method to select only those
                    countries that are in the given continent</li>
            <li>Call the filterByContinent method to find the info about countries in Oceania</li>
            <li>Save the result in a .csv file (name the file as descriptive as possible)<strong>(5 %)</strong></li>
            <li><strong>(10 %)</strong>Define a method filterByPerCapita(List<Country> countries, Double lower, Double
                    upper) method to select
                    those countries whose UN_GDP_per_capita falls in the given range </li>
            <li>Call the filterByPerCapita method to find the info about countries whose per capita gdp is in the range
                of [40000,50000] </li>
            <li>Save the result in a .csv file (name the file as descriptive as possible)<strong>(5 %)</strong>
            </li>
        </ul>
    </li>
    <li>Note: in case of an invalid field name, continent, throw a meaningful exception instance and handle it back in
        main</li>
</ul>

<h3>Task Related - Class diagrams <strong>(5 %)</strong></h3>
Draw the class diagrams including all the classes and their associations. Add the image(s) to the project
folder so that they are submitted to the repository as well. You may use any tool to draw the diagrams. Make sure you
submit image format (.jpg or .png).

<h4> Submission related: (5%)</h4>
<ul>
    <li> Record a short video not exceeding 5 minutes to explain the code
        as well as the way users can interact with the end product
        <ul>Show:
            <li> main blocks of the code base</li>
            <li> each of the features mentioned above</li>
            <li> files that are generated (discuss either in a text editor or in an Excel sheet)</li>
        </ul>
    </li>
    <li> Upload the video to YouTube and share the link by adding it to your README.md file as the first line.</li>
    <li> Submissions without a video recording will not be graded.</li>
</ul>

<h4>Important notes:</h4>
- Codes that do not compile and run for any reason will <strong>not be graded</strong>. Test properly before you submit
your work.<br />
- Please, also refer to the course syllabus about the assignments. <br />
- Each completed feature must be commited and pushed <strong>works submitted in just one or two commits are not
    acceptable</strong>. <br />
- This assignment will give you <strong><em>5 %</em></strong> of the overall. <br />