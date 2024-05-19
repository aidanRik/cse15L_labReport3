# Lab Report 3   
## Aidan Rikic

**Part1**   
I'm choosing `reversedInPlace` in `ArrayExamples`  
1.  
`@Test 
  public void testReverseInPlace2(){
    int[] exArray = { 1, 2, 3, 4, 5};
    ArrayExamples.reverseInPlace(exArray);
    assertArrayEquals(new int[]{5, 4, 3, 2, 1}, exArray);
  }`  
2.  
`@Test 
	public void testReverseInPlace() {
    int[] input1 = { 3 };
    ArrayExamples.reverseInPlace(input1);
    assertArrayEquals(new int[]{ 3 }, input1);
	}`  
3.  
![Image](labReport2_ss1.png)
![Image](labReport2_ss2.png)  
4.  
Failing code:  
`static void reverseInPlace(int[] arr) {
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = arr[arr.length - i - 1];
    }
  }`  
Working Code:  
`static void reverseInPlace(int[] arr) {
    int[] placeHolder = arr.clone();
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = placeHolder[arr.length - i - 1];
    }
  }`  
5.  
The issue with the original code was that it was changing the array as it was iterating through the array. This changes the ints in the array before they are even swapped, and therefore messes up the back half of the array. In order to fix this, we create a placeholder array and swap the numbers there `arr` isn't affected while iterating through. 

**Part2**  
1.  
Command: `grep -r`  
Directory Example:  
`aidan_rikic@Aidans-MacBook-Air docsearch % grep -r "biomed" ./technical/biomed
./technical/biomed/1471-2202-2-9.txt:        http://www.biomedcentral.com/1471-2202/2/8). It is now
./technical/biomed/1472-6882-3-3.txt:        literature search in biomedicine depends on the appropriate
./technical/biomed/1472-6882-3-3.txt:        The controlled vocabulary for biomedicine has been
./technical/biomed/1472-6882-3-3.txt:        biomedical literature [ 3 ] . With the recent development
./technical/biomed/1472-6882-3-3.txt:        Other biomedical databases that include CAM literature,
./technical/biomed/1472-6882-3-3.txt:          biomedicine and it has a subset focusing on complementary
./technical/biomed/1472-6882-3-3.txt:          biomedicine, investigators and authors in the fields of
./technical/biomed/1471-2202-2-8.txt:          paper http://www.biomedcentral.com/1471-2202/2/9), and
./technical/biomed/1472-6947-3-8.txt:          Creators of biomedical databases use terminologies to
./technical/biomed/1472-6947-3-8.txt:        biomedical data sets. Public comment is welcomed.
./technical/biomed/gb-2001-2-4-research0012.txt:        biomedicine of the visual computer language paradigm [ 24,
./technical/biomed/gb-2001-2-4-research0012.txt:        to biomedical education, investigation and industry. For
./technical/biomed/gb-2003-4-7-r46.txt:        gene annotations or concepts from the biomedical
./technical/biomed/1471-2474-2-3.txt:        http://www.biomedcentral.com/1471-8219/2/5
./technical/biomed/1475-9276-1-3.txt:        33 34 ] . This model has been widely applied in biomedical
./technical/biomed/1472-6807-1-1.txt:        types of ligands could therefore have important biomedical
./technical/biomed/1472-6920-2-3.txt:        international journals [ 5 ] . For biomedical disciplines
./technical/biomed/1471-2105-3-17.txt:        study aimed at enabling the biomedical community to cope
./technical/biomed/1471-2105-3-16.txt:        The availability of biomedical literature in electronic
./technical/biomed/1477-7827-1-54.txt:        study increases the biomedical significance of findings
./technical/biomed/1471-2164-3-7.txt:        of biomedical research. These include, but are by no means
./technical/biomed/1471-2164-3-18.txt:          in Gel/Mount (biomeda) containing 4',6
./technical/biomed/1472-6882-1-12.txt:        biomedical framework. While the SR method has been used in
./technical/biomed/1472-6947-3-5.txt:        another level of biomedical data integration in which array
./technical/biomed/gb-2003-4-4-r28.txt:        biomedical research community. GoMiner is flexible both`  

Explanation: The `grep -r` command allows us to search recursively through certain directories and their subdirectories for files that contain the specific string given.  

File Example:  
`aidan_rikic@Aidans-MacBook-Air docsearch % grep -r "biomed" ./technical/biomed/1471-2202-2-9.txt 
./technical/biomed/1471-2202-2-9.txt:        http://www.biomedcentral.com/1471-2202/2/8). It is now`  

Explanation: When we add a file to the end of the path, the `grep -r` command only searches through that specific file. This makes it a little less meaningful then searching through all the directories.  

2.  
Command: `grep -rn`  
Directory example:  
`aidan_rikic@Aidans-Air docsearch % grep -rn "Americans" ./technical/plos
./technical/plos/pmed.0010039.txt:9:        agree that this level of spending should be more than enough to provide all Americans with
./technical/plos/pmed.0010039.txt:11:        goals. What are the flaws in the United States health system that prevent Americans from
./technical/plos/pmed.0010039.txt:23:        policies may deprive tens of millions of Americans access to affordable care. The AMA
./technical/plos/pmed.0010039.txt:35:        There are 45 million Americans with no health care coverage, and not surprisingly, lack
./technical/plos/pmed.0010039.txt:54:        Inadequate insurance coverage is making average-income Americans poorer. A recent study
./technical/plos/pmed.0020062.txt:25:        African-Americans and other racial and ethnic minorities.
./technical/plos/pmed.0020062.txt:102:        of conditions prevalent among African-Americans, such as sickle cell disease and prostate
./technical/plos/pmed.0020062.txt:115:        specifically designed for the treatment of congestive heart failure in African-Americans
./technical/plos/pmed.0010058.txt:125:        limited donor pool. The numbers are striking; at least 1 million Americans have T1DM, and
./technical/plos/pmed.0010058.txt:151:        transplant. With over 1 million Americans dealing with T1DM, it would cost over $100
./technical/plos/pmed.0020149.txt:32:        clinical characteristics, with lower usage in younger patients, females, African-Americans,
./technical/plos/pmed.0020002.txt:116:        factors, particularly among African-Americans and Filipinos [25]. Pregnancy is also a risk
./technical/plos/pmed.0010052.txt:177:        It's no secret that many Americans are deeply ashamed of their personal shortcomings and
./technical/plos/pmed.0010045.txt:134:          sample was composed of 59% Caucasians and 35% African-Americans. All participants were
./technical/plos/journal.pbio.0020439.txt:269:          culture of the Native Americans of the northwest coast of North America. In the case of
./technical/plos/journal.pbio.0020404.txt:18:        its usual low doses. Native Americans chewed tobacco to treat intestinal symptoms, and in
./technical/plos/pmed.0020123.txt:201:        Americans with existing CHD would benefit from drug therapy to achieve the target LDL-C
./technical/plos/pmed.0020123.txt:220:        Nutrition Examination Survey III data showed that 60% of 38.5 million adult Americans
./technical/plos/pmed.0020123.txt:260:        African-Americans, and patients cared for by non-cardiologists. These findings may be
./technical/plos/pmed.0020082.txt:17:        African-Americans have about four times the risk of AD of native Nigerians. If genetics
./technical/plos/pmed.0010034.txt:8:        errors may kill nearly 100,000 Americans every year [1], United States health care experts`  

Explanation: the command `grep -rn` searches recursively through the directory `./technical/plos` for the given string `Americans` and returns the path and line number of each instance it finds

File example:  
`aidan_rikic@Aidans-Air docsearch % grep -rn "American" ./technical/plos/journal.pbio.0020001.txt 
./technical/plos/journal.pbio.0020001.txt:32:        represents North American and European publications far better than those of the rest of
./technical/plos/journal.pbio.0020001.txt:81:        of its resources in scientific research and development. Latin American investment in
./technical/plos/journal.pbio.0020001.txt:84:        Among Latin American countries, there is a high degree of variability in publication
./technical/plos/journal.pbio.0020001.txt:134:        For the top 20 ecological journals, the American subcontinents of South, Central, and
./technical/plos/journal.pbio.0020001.txt:139:        the top 11–20 (impact factors 3.28–2.47), the Latin American countries contributed nearly
./technical/plos/journal.pbio.0020001.txt:158:        American researchers are not shying away from the two top-ranked general science journals.
./technical/plos/journal.pbio.0020001.txt:165:        American institution was included in the remaining 6%. Overall, these data indicate that
./technical/plos/journal.pbio.0020001.txt:173:        they are the exception. Why, in general, do Latin American scientists often fail to reach`  

Explanation: the command `grep -rn` searches recursively through the file `journal.pbio.0020001.txt` for the string `American` and returns the path and the line number of each instance it finds  

3.  
Command: `grep -rl`  
Directory example:  
`aidan_rikic@Aidans-Air docsearch % grep -rl "Boston" ./technical/911report
./technical/911report/chapter-13.4.txt
./technical/911report/chapter-13.5.txt
./technical/911report/chapter-13.2.txt
./technical/911report/chapter-2.txt
./technical/911report/chapter-1.txt
./technical/911report/chapter-6.txt
./technical/911report/chapter-7.txt
./technical/911report/chapter-8.txt`  

Explanation: The command `grep -rl` searches recursively through the directory `./technical/911report` for the string `Boston` and returns the paths of the files that contain it  

File example:  
`aidan_rikic@Aidans-Air docsearch % grep -rl "Boston" ./technical/911report/chapter-1.txt 
./technical/911report/chapter-1.txt`  
	
Explanation: The command `grep-rl` is basically checking if the file `chapter-1.txt` contains the string `Boston`

4.  
Command: `grep -rL`  
Directory example:  
`aidan_rikic@Aidans-Air docsearch % grep -rL "Boston" ./technical/911report
./technical/911report/chapter-13.1.txt
./technical/911report/chapter-13.3.txt
./technical/911report/chapter-3.txt
./technical/911report/chapter-5.txt
./technical/911report/chapter-9.txt
./technical/911report/preface.txt
./technical/911report/chapter-12.txt
./technical/911report/chapter-10.txt
./technical/911report/chapter-11.txt`  

Explanation: The command `grep -rL` works oppositely to `grep -rl` as it recursively searches through the directory `./technical/911report` for the string `Boston` and returns the paths of the files that don't contain it

File example:  
`grep -rL "Boston" ./technical/911report/chapter-1.txt`  
	
Explanation: This line should return nothing as the file `chapter-1.txt` contains the string `Boston`. Therefore this command could be used to check if a file contains a string. 



  



