# TechDivision.Jobs.ApplicationForm
This is a default application form implementation based on [neos/form-builder](https://github.com/neos/form-builder) with fields that are quite often used.
It will install the package [techdivision/form-encryption](https://github.com/techdivision/form-encryption) to enable secure communication.
Sending applicant data via e-mail can be non GDPR-compliant for a company.   

### Installation

TechDivision.Jobs.ApplicationForm is available via packagist. Add `"techdivision/jobs-applicationform" : "~1.0"` to the require section of the composer.json
or run `composer require techdivision/jobs-applicationform`.  

## NodeTypes
### ApplicationForm  
Fully featured application form with many default fields - so you dont have to build it yourself.
If you want to adapt the form to your needs, please override the Fusion prototype `TechDivision.Jobs.ApplicationForm:ApplicationForm`.
We recommend to add the "EncryptedEmailFinisher" for sending the form
#### Email  
You can use the file [Admin.html](https://github.com/techdivision/jobs-applicationform/tree/master/Resources/Private/Templates/Mails/Admin.html) 
either as `templatePathAndFileName` option or as `templateSource` within the EncryptedEmailFinisher NodeType.

### JobSelect
You can as well add your own NodeBased Form and build your own Application Form.  
For this purpose, we added a JobSelect FormElement. This NodeType will display a select (dropdown) with all available JobPostings

### ApplicationButton
For the applicant journey we would like to connect the JobPosting with the ApplicationForm.  
Therefore you have a button "Apply now", which will
- link to the ApplicationForm 
- Add the current JobPosting as get parameter
- display only the requested JobPosting in the JobSelect

## Further packages
To make jobs complete, we do offer a set of packages:
* [techdivision/jobs](https://github.com/techdivision/jobs)  
Basic job package with schema.org markup
* [techdivision/card-jobs](https://github.com/techdivision/card-jobs)  
Visual card style for jobs (see also [techdivision/card](https://github.com/techdivision/card))
* [techdivision/jobs-googleapi](https://github.com/techdivision/jobs-googleapi)  
Tell google if you have new jobs, important changes or if a job has been deleted 
* [techdivision/form-encryption](https://github.com/techdivision/form-encryption)  
PGP/GPG form encryption to meet data protection standards 

### Contribution
We will be happy to receive pull requests - dont hesitate!


