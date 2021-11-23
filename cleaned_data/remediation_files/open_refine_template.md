**Prefix:**

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```



**Body:**

```
<mods>

<identifier type="pid">{{cells["PID"].value}}</identifier>
<identifier type="local">{{cells["identifier"].value}}</identifier>

<titleInfo><title>{{cells["title"].value}}</title></titleInfo>

{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}

{{if(isBlank(cells["dateCreated"].value),'','<originInfo><dateIssued>' + cells['dateCreated'].value + '</dateIssued></originInfo>')}}
{{if(isBlank(cells["dateCreated_edtf"].value),'','<originInfo><dateIssued encoding="edtf">' + cells['dateCreated_edtf'].value + '</dateIssued></originInfo>')}}

<language><languageTerm authority="iso639-2b" type="text">{{cells['language'].value}}</languageTerm></language>

<physicalDescription><form authority="aat" valueURI="http://vocab.getty.edu/aat/300311670">booklets</form><form authority="aat" valueURI="http://vocab.getty.edu/aat/300026657">periodicals</form></physicalDescription>

{{if(isBlank(cells['subject_name'].value), '', '<subject'+ if(isBlank(cells['subject_name_URI'].value), '', ' valueURI="' + cells['subject_name_URI'].value + '"' + ' authority="wikidata"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}

<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n90646627"><name><namePart>Tennessee Volunteers (Football team)</namePart></name></subject>

{{if(isBlank(cells['subject_name_1'].value), '', '<subject'+ if(isBlank(cells['subject_name_1_URI'].value), '', ' valueURI="' + cells['subject_name_1_URI'].value + '"' + ' authority="naf"') + '><name><namePart>' + cells['subject_name_1'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['subject_topic'].value), '', '<subject' + if(isBlank(cells['subject_topic_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_URI'].value + '">') + '<topic>' + cells['subject_topic'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_topic_2'].value), '', '<subject' + if(isBlank(cells['subject_topic_2_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_2_URI'].value + '">') + '<topic>' + cells['subject_topic_2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_topic_3'].value), '', '<subject' + if(isBlank(cells['subject_topic_3_URI'].value), '>', ' authority="lcsh" valueURI="' + cells['subject_topic_3_URI'].value + '">') + '<topic>' + cells['subject_topic_3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_topic_4'].value), '', '<subject' + if(isBlank(cells['subject_topic_4_URI'].value), '>', ' authority="wikidata" valueURI="' + cells['subject_topic_4_URI'].value + '">') + '<topic>' + cells['subject_topic_4'].value + '</topic></subject>')}}

<subject><topic>{{cells['subject_topic_5'].value}}</topic></subject>

<subject authority="naf" valueURI="http://id.loc.gov/authorities/names/n79109786"><geographic>Knoxville (Tenn.)</geographic><cartographics><coordinates>35.96064, -83.92074</coordinates></cartographics></subject>

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<relatedItem displayLabel="Project" type="host"><titleInfo><title>{{cells['relatedItem'].value}}</title></titleInfo></relatedItem>

<recordInfo><recordContentSource valueURI="{{cells['source_URI'].value}}">{{cells['source'].value}}</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['accessCondition_URI'].value}}">{{cells['accessCondition'].value}}</accessCondition>
</mods>
```



**Suffix:**

```
</modsCollection>
```

