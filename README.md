# x-dtd
Generate dtd file from database schema

This will be used for imports to xTuple - existing xtupleapi.dtd is out-of-date


Making use of the project, https://github.com/SweetIQ/schemats. Learning typescript as I go.
This is what is generated for the api.contact view:

export namespace contactFields {
    export type contact_number = string | null;
    export type honorific = string | null;
    export type first = string | null;
    export type middle = string | null;
    export type last = string | null;
    export type suffix = string | null;
    export type initials = string | null;
    export type crm_account = string | null;
    export type active = boolean | null;
    export type job_title = string | null;
    export type voice = string | null;
    export type alternate = string | null;
    export type fax = string | null;
    export type email = string | null;
    export type web = string | null;
    export type contact_change = string | null;
    export type address_number = string | null;
    export type address1 = string | null;
    export type address2 = string | null;
    export type address3 = string | null;
    export type city = string | null;
    export type state = string | null;
    export type postal_code = string | null;
    export type country = string | null;
    export type notes = string | null;
    export type address_change = string | null;

}

export interface contact {
    contact_number: contactFields.contact_number;
    honorific: contactFields.honorific;
    first: contactFields.first;
    middle: contactFields.middle;
    last: contactFields.last;
    suffix: contactFields.suffix;
    initials: contactFields.initials;
    crm_account: contactFields.crm_account;
    active: contactFields.active;
    job_title: contactFields.job_title;
    voice: contactFields.voice;
    alternate: contactFields.alternate;
    fax: contactFields.fax;
    email: contactFields.email;
    web: contactFields.web;
    contact_change: contactFields.contact_change;
    address_number: contactFields.address_number;
    address1: contactFields.address1;
    address2: contactFields.address2;
    address3: contactFields.address3;
    city: contactFields.city;
    state: contactFields.state;
    postal_code: contactFields.postal_code;
    country: contactFields.country;
    notes: contactFields.notes;
    address_change: contactFields.address_change;

}




This is what we're looking for:

<!ELEMENT contact ( contact_number?,
		    honorific?,
		    first?,
		    last?,
		    initials?,
		    crm_account?,
		    active?,
		    job_title?,
		    voice?,
		    alternate?,
		    fax?,
		    email?,
		    web?,
		    address1?,
		    address2?,
		    address3?,
		    city?,
		    state?,
		    postal_code?,
		    country?,
		    address_change?,
		    notes? ) >
<!ATTLIST contact	mode	(insert|update)	'insert'
			ignore 	(true|false)	'false'
			key	CDATA	#FIXED	'contact_number' >
