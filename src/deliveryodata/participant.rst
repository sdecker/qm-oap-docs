Participant
-----------

..  od:service::    deliveryodata

..  od:type::   Participant

    ..  od:prop::   ID  Edm.Int32
        :key:
        :notnull:

        The numeric ID of the Participant.

    ..  od:prop::   Name  Edm.String

        The name of the Participant. See
        :qm:field:`G_Participant.Participant_Name`.
            
    ..  od:prop::   FirstName  Edm.String

        The first name of the Participant.  See
        :qm:field:`G_Participant.First_Name`.
            
    ..  od:prop::   LastName  Edm.String

        The last name of the Participant.  See
        :qm:field:`G_Participant.Last_Name`.
            
    ..  od:prop::   MiddleName  Edm.String

        The middle name of the Participant.  See
        :qm:field:`G_Participant.Middle_Name`.

    ..  od:prop::   PrimaryAddress1  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryAddress2  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryCity  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryState  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryZIPCode  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryCountry  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryPhone  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryFax  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PrimaryEmail  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryAddress1  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryAddress2  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryCity  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryState  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryZIPCode  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryCountry  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryPhone  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryFax  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   SecondaryEmail  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Salutation  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   OrganizationName  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Department  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Title  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   AssistantName  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   ManagerName  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Gender  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   URL  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details  Edm.String

        The details field.  See :qm:field:`G_Participant.Details`.
        Often used to contain a human-friendly representation of the
        participant's full name.
            
    ..  od:prop::   Details1  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details2  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details3  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details4  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details5  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details6  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details7  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details8  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details9  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details10  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details11  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details12  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details13  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details14  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details15  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details16  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details17  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details18  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details19  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   Details20  Edm.String

        .. versionadded:: 2017.11

    ..  od:prop::   PreferredLang  Edm.String

        .. versionadded:: 2017.11
            
    ..  od:prop::   RegistrationDateTime  Edm.DateTime
        :notnull:
        
        The date and time when the participant was first registered.
        Sourced from :qm:field:`G_Participant.Date_Registration` but
        converted to UTC.

    ..  od:prop::   Groups Group
        :collection:
        
        Navigation property to the Groups this participant is a member
        of.

    ..  od:prop::   Schedules Schedule
        :collection:

        .. versionadded:: 2017.11
        
        Navigation property to the Schedules related to this participant
    
    ..  od:action:: ActionableSchedules ActionableSchedule
        :collection:

        .. versionadded:: 2017.11

        Returns a collection of :od:type:`ActionableSchedule` related to
        this participant.  It takes no parameters and is bound to a
        specific Participant so is called like this::
        
            POST /deliveryodata/<customer-id>/Participant(123456)/ActionableSchedules
            
            {
            }
        
        A Schedule is *actionable* if the Participant can take some
        action in relation to it (typically start or resume).  If there
        are no actionable schedules an empty value is returned as
        follows::

            Content-Type: application/json; charset=utf-8

            {
                "odata.metadata": "https://ondemand.questionmark.eu/deliveryodata/<customer-id>/$metadata#Collection(QM.DeliveryODataService.DTO.ActionableSchedule)",
                "value": []
            }        

    ..  od:action:: ActionableSchedule ActionableSchedule
        :input: ScheduleID Edm.Int32

        .. versionadded:: 2017.11

        Returns a single :od:type:`ActionableSchedule` related to
        this participant and the Schedule referred to in the input
        parameter.
        
        It is called like this::
        
            POST /deliveryodata/<customer-id>/Participant(123456)/ActionableSchedule
            
            {
                "ScheduleID": 12345
            }
        
        See :od:action:`ActionableSchedules` for more information.
       
