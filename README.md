<img width="1378" alt="Screen Shot 2021-10-06 at 3 51 30 PM" src="https://user-images.githubusercontent.com/87823308/136273501-236670c3-3d61-4f06-927a-ff21c05d7fb3.png">

## The Personal Chronicle aka "personicle" . The Personicle is a person centric healthcare data platform that registers Individual events of lifestyle, health, social, environmental, and other related events to provide highly personalized  & preventive health insights in real time.

## Introduction

Personicle is a personal chronicle of lifestyle, health, social, environmental, and other events and all associated information and data for a person.  A Personicle is a time-indexed database of events and their attributes for a person.  Earlier versions of such systems with limited applications and scopes have been called lifelog and digital twins.  
A Personicle System (referred to as PS), however, is a collection of Personicles available for the benefit of a population or society.  Better disease models could be built for sub-populations by aggregating individuals in a population that share certain individual attributes (for e.g., all people of Indian origin in their sixties, living in southern California, working in academic fields).  Thus, many different population groups may be studied based on appropriate collection of individuals.
Increasing emphasis in health-related disciplines is on developing personalized, predictive, precise, and participatory approaches to guide people to manage their future in most desirable way to maximize quality of health leading naturally to better quality of life.  In health, Personalized, Predictive, Preventive, and Precise approaches to managing health are rapidly gaining popularity.  These approaches, commonly called P4, or Px, in healthcare, primarily depend on building a person’s model and using it to predict potential health issues in future to prevent them using precise guidance specifically customized for the person.  
P4 approaches depend on the personal model.  Every guidance or recommendation system uses current state and personal model. Personal models have been and are being used extensively in most popular consumer applications in this century.  All search engines, shopping sites, and social networks build personal profiles based on interactions with the person on their site.  They collect logs of relevant data from interactions with every user on their site and from any other relevant information sources for their application.  These logs are then used to build personal profiles or personal models for their use.  Once built, this profile is used to help in search or recommendation as well as targeting advertisements for company’s monetization.  For health, the personal model must be derived using an objective log of person’s genome, lifestyle activities, environmental exposures (called exposomes), and accurate biological measurements.  Each person’s body reacts differently to the same lifestyle actions, exposome, and social inputs.  A personal model captures effects of all these factors on the individual’s health by relating health related biomarkers and inputs from the person to all events surrounding the person.  This personal model is essential in predicting and guiding the person based on their current health state and context.  The most challenging component in this is building a good quality Personicle of the person and then build the personal model using event mining or other related AI tools and medical/biological knowledge.  Good models require good quality and detailed logs of data that could be analyzed to build quality models.  Paraphrasing a popular saying of computer science: poor logs (garbage in); poor models (garbage out).

Personicle makes this process of collecting logs of all relevant data streams for understanding and building personal model or personal profile explicit and could be designed for specific health and other applications.  Most data streams must be converted to semantic events in them.  The events may be of different types, such as events in a data stream, or events in life derived from multiple data streams or supplied by an individual source.  All these events may be explicitly represented in Personicle using an event model that provides more information about an event.  
Personal models must have two very important attributes: human-understandability, and predictive power.  Predictive power is essential to understand future implications of the current states (contexts) for the individual and human understandability requires representing causality that people can understand and use.  People understand life events and features of these events and can relate to those.  For human-understandability, it is essential to convert all logged data to common life-events and their features and use event mining techniques to build personal models.

A Personicle may be created either for a specific application over a limited period, or it may be an exhaustive chronicle of all events from pre-natal to passing of the person.  Essentially a Personicle is a person centered, event indexed, chronicle containing all relevant data about a person over a certain time-period and for specific applications.
A Personicle for health applications is created to keep a record of all data streams related to a person and life events derived from this data to apply appropriate machine learning, AI, and other analytical approaches to create a model of a person that could be used for monitoring health, for providing information to healthcare providers about health of the person, and for creating a model of person for applying predictive, preventive, precise, and personalized approaches.  Currently, all these tasks are performed using shallow episodic data, resulting in misdiagnosis and inappropriate treatment of health.  A Personicle brings power of sensors and data-driven approaches to provide right and precise information to right stakeholders in right context.
An important objective of Personicle is to provide an environment to collect data from diverse data streams and other data sources centered on and about a person.  All data about the person is synchronized and stored in a form for different applications to use as needed by them and permitted by the user.  The primary owner of their data is the person.  The person decides what data should be collected, what kind of processing may be permitted using this data, and who may have access to different data items during different periods.
A personicle is a log of all relevant data for a person indexed using semantic events.  This allows for modeling a person in the context of managing specific aspect of her life using predictive approaches to provide recommendations to maximize quality of experiences. Indexing using human understandable semantic events is important for human interaction and allows us to use events as a bundle of all information and data. These events should be automatically detected so that minimal interaction is required on the part of a user.

### Goal

A Personicle is a chronicle of all events for the person.  These events will be used to build their ‘model’ for understanding the underlying causes for various health outcomes: what caused the food allergy, or what resulted in major emotional upset.  
Such a model combined with current situation, may help in prediction of future situations as well as ways to prevent those situations.  
For each person, there will be a core Personicle.  Different applications may add many more data sources, events, and algorithms to extract more relevant information that will be added to the core Personicle.

### Requirements

**Synchronization and Sampling**:  Different data streams come from different sensors and may have different sampling rates and different attributes as their values.  All these must be put on the system’s time clock and their sampling should be compared and adjusted for assimilating these streams with other streams as may be required.  
**Time period for Personicle**:  If relevant, store the duration of the Personicle.
1.	Start date, end date (if any)
2.	Special circumstances
3.	Special observations
4.	Special situations to be monitored  

**Differential Access to data**: Different applications and human experts could leverage the Personicle to provide improved and personalized services to the end-user. We need to design data sharing protocols and mechanisms for the system that allows for such data sharing while at the same time preserving user privacy and ensuring that external services only access the data they require (and the user has granted access).

## TYPES OF PERSONAL DATA

Data is essential for deriving information and knowledge for human life and society.  Data from multimodal diverse sources must be collected and perpetually analyzed to build model of the person and understand health state of a person as well as society.  Many diverse distributed sources contribute to this.  These sources may be grouped into following classes: 

### PERSONAL INFORMATION

These include general information about a person that do not change frequently. These can be viewed as user demographic features and can be used to identify groups or sub-populations of similar users. Some examples of these features are:
1.	Name
2.	Residential Address 
3.	Profession
4.	Chronic Health Conditions and Allergies
5.	Ethnicity
6.	Family members

### GENOMIC DATA

Genomic information about the users can provide valuable insights into their health behavior and outcomes. DNA testing and genetic sequencing have gained popularity in the last few years due to readily available consumer grade sequencing (e.g., 23andme). These applications provide a shallow insight into user health and behavior using known genetic markers (from biomedical literature) for health and behavioral outcomes.  
The Personicle should leverage this information to provide a deeper and more accurate view of individual health and behavioral outcomes. However, due to the differences in scale, structure, and utility of the genomic data, we need to process and store it separately from the other demographic and individual level features.

### LIFE SITUATIONS

Situations in a personal context are a specific combination of events and states that hold special significance in the application domain.  Typically, the situations last over significantly longer durations than events and impact the events that occur during the situation. For example, “SAT preparation” is one possible situation for a high school student and is likely to lead to a change in observed distribution of life events.  
In many health cases, situations may refer to diseases that need attention and determine the relative importance of different events and data streams. 
A situation may need following information: 
1.	Name of situation
2.	Intensity of situation
3.	Any actions required
4.	People to be informed 

### EVENTS

Our day-to-day lives are structured into different time intervals and instances that represent significant activities or Events. Events provide a natural, semantically meaningful, and easy to understand abstraction over raw data collected for an individual. The event abstraction allows us to reason with daily life activities and not worry about underlying sensor modalities and data quality. Therefore, as newer and better sensing methods are developed for different aspects of life, we can devise event recognition modules for these modalities. This allows us to seamlessly integrate latest sensors and devices in the Personicle without impacting the event-driven layers.
We will discuss the different types of user events that we should collect in their Personicle and the possible sources for such events.

#### REGULAR LIFE EVENTS

These are the events detected by application programmers by combining multiple relevant streams to detect meaningful life events.  Life-events are basic events in human life and may be defined by an application.  These life events may be computed using specific data and other event streams.  These may also be reported or recorded by the user via specific applications.  
Additionally, each life event also includes event specific information that describe different aspects of the event. These include:
1.	Location: (latitude, longitude, altitude) and Places of interest (Type)
2.	Time: (start time: end time); duration
3.	Type of Event: all relevant info for this specific type
    1.	Participants, 
    2.	Event Name or Activity performed

<!--   3.	… -->
4.	Sub-events: Other events that may be contained in this event
5.	Causality: What may have caused this event.
6.	Data and feature streams relevant to this event (– GPS, Heart rate, activity, food, Blood glucose level, …)
7.	Event-specific Info: (Event Name, event specific info such as distance for Running events)

Personicle should include event recognition and event retrieval operations for commonly observed life events such as eating, sleeping, and working. Many applications already recognize a subset of these life events, and we should leverage these sources for creating the personicle.

#### EPISODIC EVENTS

Many interesting events about a person may be imported from their calendar, email, or social media.  For health applications, a major source maybe EHR listing their diagnostic tests, doctor’s opinions, medical prescriptions and other health related events and observations.  These should be imported in the Personicle and should be used to assimilate with data streams to build and enrich the Personicle.

#### DATA STREAMS

Raw data or observations from different sensors and related application are stored as data streams in a system as time indexed data.  In some cases, the system may also detect events in data streams and store such event streams also.  Event streams may be directly obtained using a device, an application, or a human observer.  Both data and event streams may be used for later analysis as well as visualization purpose.  The data and events obtained using a sensor or observer are original data and should be maintained as data that cannot be altered.  One may compute other events and features using these, but original data and events should be maintained.  For all individual data streams Personicle records: 
1.	Source of data stream: Observer, sensor, or a data source
2.	Type of data: numbers, classes, …
3.	Periodicity: Episodic, Continuous (frequency)
4.	Uses: used to derive activities, events, situations
5.	Data-Used-In:  specific activity or events using this stream.
6.	Data Stream: <Time, Value>

#### SOCIAL DETERMINANTS OF HEALTH

Social Determinants of Health (SDOH) have been defined as the “conditions in which the individuals live, learn, work and play”. These conditions have a great impact on health and quality of life risks and outcomes and contribute to various chronic disease risk factors such as stress, access to clean water and electricity, access to healthcare etc. These features can be readily accessed from servers and datasets maintained by government agencies (such as CDC) and matched with users’ home and work location.  
Possible Sources:

|Data|Source|
|----|-------|
|Chronic disease indicators | https://www.cdc.gov/cdi/index.html |
|Places | https://www.cdc.gov/places/ |
|Atlas of Heart disease and stroke | https://nccd.cdc.gov/dhdspatlas/ |
|National Environmental and Public Health tracking | https://ephtracking.cdc.gov/showHome.action |
|Social Vulnerability Index | https://www.atsdr.cdc.gov/placeandhealth/svi/index.html |

These are typically available in form of GIS layers and can be easily incorporated in a geolocation indexed database. The users’ home, work or similar locations of interest can be used to populate these features for them.

#### EXPOSOME

Exposome for an individual incorporates different environmental exposures encountered during day-to-day lives. These exposures can affect a person’s long-term and short-term health. Repeated exposures may even affect a person’s gene expressions, also known as epigenetic changes. Like SDOH, environmental data (including weather and pollutants) is continuously collected by various government bodies all over the world. This data is aggregated by Environment Protection Agency (EPA) in United States and is freely available for everyone.  
We can use the continuously collected location stream for a user to compute their exposure to various pollutants over time and utilize it as we would use any other stream in the Personicle.  
Possible Sources:
|Data|Source|
|----|------|
|Air Pollution Streams | https://www.airnow.gov/ |

### SYSTEM ARCHITECTURE




### DATA COLLECTION

We need to leverage a variety of data sources for creating a holistic personicle. These include (but are not limited to) smart phone, smart watches (on-device sensors), medical devices, research-grade sensors, smart phone applications and GPS systems. The personal data can be further enriched using freely available public information such as weather and pollution data.  
Data generated by the individuals can be categorized along different dimensions. We primarily categorize different types of data based on their generation mechanism.  The data generation frequency determines whether a particular data stream is continuous, periodic, or episodic.  Additionally, the data generating source determines whether the data are objective, subjective, or derived from another objective or subjective data.  

Continuous data represents data streams that are continuously being generated by a device irrespective of the user activity. These include data collected from the sensors and devices such as accelerometer, temperature, heart rate etc. These are typically objective or derived as it is difficult for human agents (users or observers) to continuously report data.  
Periodic data refers to data that are not continuous but are generated after periodic intervals. These can be subjective, objective, or derived.  
Episodic data refers to data that are generated in an episodic manner and may be associated with occurrences of some events. These can include data related to Electronic Health Records (EHR) and other clinical measures that are taken sporadically but have very high accuracy and can be valuable.

These categorization of different data streams and events determine how we collect, store and process data and will be utilized in the further modules of the system. Data generation frequency determines the storage that will be used for efficiently storing and processing the data and the objectivity (or accuracy) of the data determines how different algorithms and applications will use the stored data.

|	| Episodic | Periodic | Continuous|
|-----|-----|-----|-----|
|**Subjective** | Self-reported pain | Self-reported Sleep quality | NA |
|**Objective** | Diagnostic reports | Circadian (Sunrise, sunset, wakeup time) | Accelerometer stream, Location stream |
|**Derived** | Diagnosis (EHR) | Sleep Events (from smart watch) | Heart rate stream, steps stream|

#### PRIMARY DATA SOURCES

As discussed above, a user’s Personicle is primarily populated using data from different sensor, devices, and smartphone, and can be further enriched using publicly available data. All consumer grade sensors publish their data to a cloud-based server or a local hub (usually a smartphone), which is further processed to derive user metrics and then displayed to the user. Therefore, it makes sense to utilize the data from these sources (Derived data streams) which can be accessed in the smart phones or using API access.  
However, we would also benefit from collecting the raw sensor data from the devices, which are typically not available through data export mechanisms or API access. We need to develop applications for Android, iOS platforms, and various wearable platforms (such as WearOS, Garmin, Fitbit etc.) for collecting objective sensor data directly from the devices. These on device applications can communicate with the smart phone application for periodically transferring sensor data. This also provides us a channel for incorporating future sensors that communicate with smart devices using popular data transfer protocols such as Ant+ or Bluetooth. Such devices can be registered with the Personicle smart phone application and collect data when the devices are active.  
The smartphone application should collect data periodically different sensors (on smart phone and other connected devices) and push it to a cloud-based system which acts as the integrated backend for the Personicle.  
The high-level interactions between these applications are illustrated in the figure below.
![Data Collection Workflow](https://user-images.githubusercontent.com/28337389/134455672-661ef84d-cc40-4462-a07e-3ca2e33376e6.png)

#### SDOH + EXPOSOME SOURCES

SDOH and Exposome data are dependent on the user’s location history and can be derived in the personicle backend using the public sources discussed above.

### DATA MANAGEMENT

Personicle should manage observations, derived events and their attributes, other events, and attributes such that different stakeholders may access them and use event related attributes for their own applications.  It is expected that many applications may want to get data or even contribute data and algorithms to Personicle.  Data model, query environment, and long-term storage management abilities of Personicle should facilitate this.

#### DATA MODEL

Stream Features: Each data stream may be analyzed for specific application to detect features in it.  For example, heart rate has a numerical value at any time, but in specific applications, heart rate may be classified as very low, low, normal, high, and very high using a specific algorithm that may even consider the person and the heart rate and activity or context at the time.  For each stream, such features may be calculated, and the stream may be converted to such feature stream.  In some cases, the sensor or observer may directly give feature values over time. For all data streams, we may have feature streams calculated and the following attributes recorded:  
1.	Name.
2.	Derived-or-observed: If derived then observation stream.
3.	Activity: <time interval, activity>

### EVENT RECOGNITION AND RETRIEVAL

#### DATA-DRIVEN EVENT RECOGNITION

#### INTERACTIVE EVENT RECOGNITION

### DATA SHARING PROTOCOLS

Some stakeholders may want to explore and analyze Personicle from their application view and should be able to access only a limited subset of Personicle.  These applications may want to create an environment in which their private data may be combined with Personicle to offer them an environment very specific to their application.

#### STAKEHOLDERS IN THE SYSTEM
1.	Individual users
2.	Healthcare Professionals
    1.	Providers
    2.	Insurance
    3.	Employer

3.	Application developers

## Our Product Roadmap
<img width="1647" alt="Screen Shot 2021-10-06 at 3 56 21 PM" src="https://user-images.githubusercontent.com/87823308/136274193-70248671-9577-4a12-815b-6f9b9e62d6f3.png">

![clearsense-logo](https://user-images.githubusercontent.com/87823308/136274577-c41c4a72-7a79-425a-b977-ab7bacad1f5d.png)

