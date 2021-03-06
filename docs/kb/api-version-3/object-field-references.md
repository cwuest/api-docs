# Object Field References

Each field returned by the API maps to a field within the Pardot user interface. The tables in this section list all fields that can be returned and/or updated via the API. Consider the following limitations:

<ul>
<li>Fields marked as 'Editable' can be manipulated through <code>create</code>, <code>update</code>, and <code>upsert</code> requests.</li>
<li>'Required' denotes that the specified field cannot be left without a value during <code>insert</code> and some <code>upsert</code> requests. <code>update</code> requests that clear a required field will be declined.</li>
<li>During <code>update</code> requests, the parameter names submitted to the API and tag names in the API's response will match field names within the Pardot user interface unless otherwise specified.</li>
</ul>


## Campaign

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this campaign</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Campaign's name</td>
</tr>
<tr>
<td>&lt;cost&gt;</td>
<td>integer</td>
<td></td>
<td>X</td>
<td>Cost associated to the campaign</td>
</tr>
<tr>
</tr>
</table>
## Custom Field

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this custom field</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Custom field's name</td>
</tr>
<tr>
<td>&lt;field_id&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>API ID for custom field</td>
</tr>
<tr>
<td>&lt;type&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>type of field</td>
</tr>
<tr>
<td>&lt;type_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for custom field's type</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time custom field was created in Pardot; Time is reported in API user's
        preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time custom field was updated; Time is reported in API user's
        preferred timezone</td>
</tr>
<tr>
<td>&lt;is_record_multiple_responses&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If true, this custom field will record multiple responses</td>
</tr>
<tr>
<td>&lt;crm_id&gt;</td>
<td>integer</td>
<td></td>
<td>X</td>
<td>The CRM ID of the field you would like to map to this custom field</td>
</tr>
<tr>
<td>&lt;is_use_values&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If true, this custom field will use predefined values</td>
</tr>
</table>

## Custom Redirect

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this custom redirect</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Custom redirect's name</td>
</tr>
<tr>
<td>&lt;Url&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>URL for the custom redirect</td>
</tr>
<tr>
<td>&lt;destination&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>URL the custom redirect leads to</td>
</tr>
<tr>
<td>&lt;campaign&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>The campaign associated with this custom redirect</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time custom redirect was created in Pardot; Time is reported in API user's
        preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time custom redirect was updated; Time is reported in API user's
        preferred timezone</td>
</tr>
</table>

## Dynamic Content

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this dynamic content</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Dynamic content's name</td>
</tr>
<tr>
<td>&lt;embedCode&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Code to embed this dynamic content onto your webpage</td>
</tr>
<tr>
<td>&lt;embedUrl&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>URL to embed this dynamic content</td>
</tr>
<tr>
<td>&lt;baseContent&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>The default dynamic content</td>
</tr>
<tr>
<td>&lt;basedOn&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Field that this dynamic content is based on</td>
</tr>
<tr>
<td>&lt;variation&gt;</td>
<td>node</td>
<td></td>
<td></td>
<td>The variation of content prospect will see based on the field's value<br>
    <strong><em>Note:</em></strong> Information about a variation is returned in a &lt;variation&gt; node in the
    XML response.  It contains the value of the field in the &lt;comparison&gt; tag and the content of the variation
     in the &lt;content&gt; tag</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time dynamic content was created in Pardot; Time is reported in API user's
        preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time dynamic content was updated; Time is reported in API user's
        preferred timezone</td>
</tr>
</table>
## Email

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this email</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Name of this email</td>
</tr>
<tr>
<td>&lt;subject&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Email Subject</td>
</tr>
<tr>
<td>&lt;message&gt;</td>
<td>XML Object</td>
<td></td>
<td></td>
<td>Contains text and html elements of different formats</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>Timestamp</td>
<td></td>
<td></td>
<td>Time the Email Was Created</td>
</tr>
</table>
## Form

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this form</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Form's name</td>
</tr>
<tr>
<td>&lt;campaign_id&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Pardot ID of the campaign associated with this form</td>
</tr>
<tr>
<td>&lt;embed_code&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>The code used to embed the form on your webpage</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time form was created in Pardot; Time is reported in API user's
    preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time form was updated; Time is reported in API user's
    preferred timezone</td>
</tr>
</table>

## Identified Company
<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this identified company</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's name</td>
</tr>
<tr>
<td>&lt;street_address&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's street address</td>
</tr>
<tr>
<td>&lt;city&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's city</td>
</tr>
<tr>
<td>&lt;state&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's state</td>
</tr>
<tr>
<td>&lt;postal_code&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's postal code</td>
</tr>
<tr>
<td>&lt;country&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's country</td>
</tr>
<tr>
<td>&lt;email&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Identified Company's email address</td>
</tr>
</table>

## Lifecycle History
<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of this lifecycle history</td>
</tr>
<tr>
<td>&lt;prospect_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot's ID for the prospect in this stage</td>
</tr>
<tr>
<td>&lt;previous_stage_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the stage this prospect was previously in</td>
</tr>
<tr>
<td>&lt;next_stage_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the stage this prospect will be in next</td>
</tr>
<tr>
<td>&lt;seconds_elapsed&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Number of seconds for prospect to get to current stage</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time lifecycle history was created in Pardot; Time is reported in API user's
preferred timezone</td>
</tr>
</table>

## Lifecycle Stage
<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of this lifecycle stage</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Lifecycle stage's name</td>
</tr>
<tr>
<td>&lt;position&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Lifcycle stage's position in lifecycle</td>
</tr>
<tr>
<td>&lt;is_locked&gt;</td>
<td>boolean</td>
<td></td>
<td></td>
<td>If true, lifecycle stage is locked</td>
</tr>
</table>

## List
<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of this list</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>List's name (internal to Pardot)</td>
</tr>
<tr>
<td>&lt;is_public&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If true, list will show on EPC pages to prospects</td>
</tr>
<tr>
<td>&lt;is_dynamic&gt;</td>
<td>boolean</td>
<td></td>
<td></td>
<td>If true, list has prospects dynamically added to it via a set of chosen rules</td>
</tr>
<tr>
<td>&lt;title&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>List's title (visible to subscribers)</td>
</tr>
<tr>
<td>&lt;description&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>List's description</td>
</tr>
<tr>
<td>&lt;is_crm_visible&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If true, list will be visible in CRM to add or remove from</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time list was created in Pardot; Time is reported in API user's
preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time list was updated; Time is reported in API user's
preferred timezone</td>
</tr>
</table>

## List Membership

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this list membership</td>
</tr>
<tr>
<td>&lt;list_id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of the list for this membership</td>
</tr>
<tr>
<td>&lt;prospect_id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of the prospect for this membership</td>
</tr>
<tr>
<td>&lt;opted_out&gt;</td>
<td>integer</td>
<td></td>
<td>X</td>
<td>If value is 1, the prospect is unsubscribed from receiving
emails from this list</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time that this membership was created in Pardot; Time is
reported in API user's preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time that this membership was updated; Time is reported in
API user's preferred timezone</td>
</tr>
</table>

## Opportunity

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this opportunity</td>
</tr>
<tr>
<td>&lt;campaign_id&gt;</td>
<td>integer</td>
<td>X</td>
<td>X</td>
<td>Pardot ID of the campaign associated with this opportunity<br>
<strong><em>Note:</em></strong> Information about an opportunity's
campaign association is returned in a &lt;campaign&gt; node in the
XML response. However, updates to campaign associations are done by
providing campaign_id=&lt;campaign_id&gt; during an UPDATE&gt;
request. See <a href="kb/api-version-3/opportunities#xml-response-formats">XML
Response Formats</a> in <a href="kb/api-version-3/opportunities">Using
Opportunities</a> for more details.</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td>X</td>
<td>X</td>
<td>Opportunity's name</td>
</tr>
<tr>
<td>&lt;value&gt;</td>
<td>integer</td>
<td>X</td>
<td>X</td>
<td>Opportunity's value<br>
<strong><em>Restrictions:</em></strong> value must be a positive
numeric value</td>
</tr>
<tr>
<td>&lt;probability&gt;</td>
<td>integer</td>
<td>X</td>
<td>X</td>
<td>Opportunity's probability<br>
<strong><em>Restrictions:</em></strong> value must be a positive
numeric value between 0 and 100 inclusive</td>
</tr>
<tr>
<td>&lt;type&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Opportunity's type</td>
</tr>
<tr>
<td>&lt;stage&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Opportunity's stage</td>
</tr>
<tr>
<td>&lt;status&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Opportunity's status<br>
<strong><em>Restrictions:</em></strong> status must be either won,
lost, or open</td>
</tr>
<tr>
<td>&lt;closed_at&gt;</td>
<td>timestamp</td>
<td></td>
<td>X</td>
<td>Opportunity's closed date<br>
<strong><em>Note:</em></strong> if this is left blank, the
closed_at timestamp (Closed Date within the app) will not be set,
even when the Opportunity's stage, status or probability are set to
indicate opportunity closure</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time opportunity was created in Pardot; Time is reported in API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time opportunity was updated in Pardot; Time is reported
in API user's preferred timezone</td>
</tr>
</table>


## Profile

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this profile</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Profile's name</td>
</tr>
</table>

## Profile Criteria

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this profile criteria</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Profile criteria's name</td>
</tr>
<tr>
<td>&lt;matches&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>The matching status of this profile criteria with the current
prospect<br>
<strong><em>Restrictions:</em></strong> Updates may be performed by
using the values match, nomatch, or unknown</td>
</tr>
</table>

## Prospect

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this prospect</td>
</tr>
<tr>
<td>&lt;campaign_id&gt;</td>
<td>integer</td>
<td></td>
<td>X</td>
<td>Pardot ID of the campaign associated with this prospect<br>
<strong><em>Note:</em></strong> Information about a prospect's
campaign association is returned in a &lt;campaign&gt; node in the
XML response. However, updates to campaign associations are done by
providing campaign_id=&lt;campaign_id&gt; during an UPDATE&gt;
request. See <a href="kb/api-version-3/prospects#xml-response-formats">XML
Response Formats</a> in <a href="kb/api-version-3/prospects">Using
Prospects</a> for more details.</td>
</tr>
<tr>
<td>&lt;salutation&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's formal prefix</td>
</tr>
<tr>
<td>&lt;first_name&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's first name</td>
</tr>
<tr>
<td>&lt;last_name&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's last name</td>
</tr>
<tr>
<td>&lt;email&gt;</td>
<td>string</td>
<td>X</td>
<td>X</td>
<td>Prospect's email address</td>
</tr>
<tr>
<td>&lt;password&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's password</td>
</tr>
<tr>
<td>&lt;company&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's company</td>
</tr>
<tr>
<td>&lt;prospect_account_id&gt;</td>
<td>integer</td>
<td></td>
<td>X</td>
<td>Prospect's account ID</td>
</tr>
<tr>
<td>&lt;website&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's website URL</td>
</tr>
<tr>
<td>&lt;job_title&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's job title</td>
</tr>
<tr>
<td>&lt;department&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's department</td>
</tr>
<tr>
<td>&lt;country&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's country</td>
</tr>
<tr>
<td>&lt;address_one&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's address, line 1</td>
</tr>
<tr>
<td>&lt;address_two&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's address, line 2</td>
</tr>
<tr>
<td>&lt;city&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's city</td>
</tr>
<tr>
<td>&lt;state&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's US state</td>
</tr>
<tr>
<td>&lt;territory&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's territory</td>
</tr>
<tr>
<td>&lt;zip&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's postal code</td>
</tr>
<tr>
<td>&lt;phone&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's phone number</td>
</tr>
<tr>
<td>&lt;fax&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's fax number</td>
</tr>
<tr>
<td>&lt;source&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's source</td>
</tr>
<tr>
<td>&lt;annual_revenue&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's annual revenue</td>
</tr>
<tr>
<td>&lt;employees&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's number of employees</td>
</tr>
<tr>
<td>&lt;industry&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's industry</td>
</tr>
<tr>
<td>&lt;years_in_business&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Prospect's number of years in business</td>
</tr>
<tr>
<td>&lt;comments&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Comments about this prospect</td>
</tr>
<tr>
<td>&lt;notes&gt;</td>
<td>string</td>
<td></td>
<td>X</td>
<td>Notes about this prospect</td>
</tr>
<tr>
<td>&lt;score&gt;</td>
<td>integer</td>
<td></td>
<td>X</td>
<td>Prospect's score</td>
</tr>
<tr>
<td>&lt;grade&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Prospect's letter grade</td>
</tr>
<tr>
<td>&lt;last_activity_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time stamp of this prospect's latest visitor activity; Time is
reported in API user's preferred timezone</td>
</tr>
<tr>
<td>&lt;recent_interaction&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Describes the prospect's most recent interaction with
Pardot</td>
</tr>
<tr>
<td>&lt;crm_lead_fid&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Prospect's lead ID in a supported CRM system</td>
</tr>
<tr>
<td>&lt;crm_contact_fid&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Prospect's contact ID in a supported CRM system</td>
</tr>
<tr>
<td>&lt;crm_owner_fid&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Prospect's owner ID in a supported CRM system</td>
</tr>
<tr>
<td>&lt;crm_account_fid&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Account ID in a supported CRM system</td>
</tr>
<tr>
<td>&lt;crm_last_sync&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time this prospect was synced with a supported CRM
system</td>
</tr>
<tr>
<td>&lt;crm_url&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>URL to view the prospect within the CRM system</td>
</tr>
<tr>
<td>&lt;is_do_not_email&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If value is 1, prospect prefers not to be emailed</td>
</tr>
<tr>
<td>&lt;is_do_not_call&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If value is 1, prospect prefers not to be called</td>
</tr>
<tr>
<td>&lt;opted_out&gt;</td>
<td>boolean</td>
<td></td>
<td></td>
<td>If value is 1, prospect has opted out of marketing
communications</td>
</tr>
<tr>
<td>&lt;is_reviewed&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If value is 1, prospect has been reviewed</td>
</tr>
<tr>
<td>&lt;is_starred&gt;</td>
<td>boolean</td>
<td></td>
<td>X</td>
<td>If value is 1, prospect has been starred</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time prospect was created in Pardot; Time is reported in API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time prospect was updated in Pardot; Time is reported in
API user's preferred timezone</td>
</tr>
</table>
## Prospect Account

<p>Note: Prospect account fields are fully customizable. To get the
most accurate field metadata for your Pardot account, use the
describe operation on the prospectAccount API endpoint.</p>
<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of the prospect account</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td>X</td>
<td></td>
<td>The name prospect account</td>
</tr>
</table>
## Tag

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this tag</td>
</tr>
<tr>
<td>&lt;name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Tag's name</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time tag was created in Pardot; Time is reported in API user's
        preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time tag was updated; Time is reported in API user's
        preferred timezone</td>
</tr>
</table>

## Tag Object

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of the tag object</td>
</tr>
<tr>
<td>&lt;tag_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>The Pardot ID of the tag</td>
</tr>
<tr>
<td>&lt;type&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>The type of object associated with the tag</td>
</tr>
<tr>
<td>&lt;object_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>The Pardot ID of the object</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time tag was associated with the object in Pardot; Time is reported in API user's
preferred timezone</td>
</tr>
</table>
## User

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID of the user</td>
</tr>
<tr>
<td>&lt;email&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>User's email address</td>
</tr>
<tr>
<td>&lt;first_name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>User's first name</td>
</tr>
<tr>
<td>&lt;last_name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>User's last name</td>
</tr>
<tr>
<td>&lt;job_title&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>User's job title</td>
</tr>
<tr>
<td>&lt;role&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>User's role</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time user was created in Pardot; Time is reported in the API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time user was updated in Pardot; Time is reported in the
API user's preferred timezone</td>
</tr>
</table>
## Visit

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for this visit</td>
</tr>
<tr>
<td>&lt;visitor_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for the associated visitor</td>
</tr>
<tr>
<td>&lt;prospect_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for the associated prospect</td>
</tr>
<tr>
<td>&lt;visitor_page_view_count&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Number of page views for this visit</td>
</tr>
<tr>
<td>&lt;first_visitor_page_view_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time of first page view for this visit; Time is reported in API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;last_visitor_page_view_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time of last page view for this visit; Time is reported in API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;duration_in_seconds&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Length of this visit</td>
</tr>
<tr>
<td>&lt;campaign_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visit's campaign parameter utm_campaign from Google
Analytics</td>
</tr>
<tr>
<td>&lt;medium_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visit's medium parameter utm_medium from Google Analytics</td>
</tr>
<tr>
<td>&lt;source_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visit's source parameter utm_source from Google Analytics</td>
</tr>
<tr>
<td>&lt;content_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visit's content parameter utm_content from Google
Analytics</td>
</tr>
<tr>
<td>&lt;term_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visit's term parameter utm_term from Google Analytics</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time visit was created in Pardot; Time is reported in API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time visit was updated in Pardot; Time is reported in API
user's preferred timezone</td>
</tr>
</table>
## Visitor

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this visitor</td>
</tr>
<tr>
<td>&lt;page_view_count&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Number of page views by this visitor</td>
</tr>
<tr>
<td>&lt;ip_address&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's IP address</td>
</tr>
<tr>
<td>&lt;hostname&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's hostname</td>
</tr>
<tr>
<td>&lt;campaign_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's campaign parameter utm_campaign from Google
Analytics</td>
</tr>
<tr>
<td>&lt;medium_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's medium parameter utm_medium from Google
Analytics</td>
</tr>
<tr>
<td>&lt;source_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's source parameter utm_source from Google
Analytics</td>
</tr>
<tr>
<td>&lt;content_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's content parameter utm_content from Google
Analytics</td>
</tr>
<tr>
<td>&lt;term_parameter&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor's term parameter utm_term from Google Analytics</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time visitor was created in Pardot; Time is reported in API
user's preferred timezone</td>
</tr>
<tr>
<td>&lt;updated_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Last time visitor was updated in Pardot; Time is reported in
API user's preferred timezone</td>
</tr>
</table>
## Visitor Activity

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this visitor activity</td>
</tr>
<tr>
<td>&lt;prospect_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for the associated prospect</td>
</tr>
<tr>
<td>&lt;visitor_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for the associated visitor</td>
</tr>
<tr>
<td>&lt;type&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Visitor activity's type number; See listing below</td>
</tr>
<tr>
<td>&lt;type_name&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Visitor activity's type name; See listing below</td>
</tr>
<tr>
<td>&lt;details&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Details about this visitor activity such as the name of the
object associated with this activity, the search phrase used in a
site search query, etc.</td>
</tr>
<tr>
<td>&lt;email_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the email associated with this visitor
activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has an email associated with it</td>
</tr>
<tr>
<td>&lt;form_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the form associated with this visitor activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a form associated with it</td>
</tr>
<tr>
<td>&lt;form_handler_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the form handler associated with this visitor
activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a form handler associated with it</td>
</tr>
<tr>
<td>&lt;site_search_query_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the site search query associated with this visitor
activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a site search query associated with it</td>
</tr>
<tr>
<td>&lt;landing_page_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the landing page associated with this visitor
activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a landing page associated with it</td>
</tr>
<tr>
<td>&lt;paid_search_id_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the paid search ad associated with this visitor
activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a paid search ad associated with it</td>
</tr>
<tr>
<td>&lt;multivariate_test_variation_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the multivariate test variation associated with
this visitor activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a multivariate test variation associated with
it</td>
</tr>
<tr>
<td>&lt;visitor_page_view_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the visitor page view associated with this visitor
activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a visitor page view associated with it</td>
</tr>
<tr>
<td>&lt;file_id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID of the file associated with this visitor activity<br>
<strong><em>Note:</em></strong> This node will only appear if this
visitor activity has a file associated with it</td>
</tr>
<tr>
<td>&lt;campaign&gt;</td>
<td>object</td>
<td></td>
<td></td>
<td>Campaign information including id, name, and cost.</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time that visitor activity occurred; Time is reported in API
user's preferred timezone</td>
</tr>
</table>
<p><a name="visitor-activity-types" id=
"visitor-activity-types"></a><br>
Visitor Activities may have the following values for
<code>&lt;type&gt;</code>:</p>
<ul>
<li>1 - Click</li>
<li>2 - View</li>
<li>3 - Error</li>
<li>4 - Success</li>
<li>5 - Session</li>
<li>6 - Sent</li>
<li>7 - Search</li>
<li>8 - New Opportunity</li>
<li>9 - Opportunity Won</li>
<li>10 - Opportunity Lost</li>
<li>11 - Open</li>
<li>12 - Unsubscribe Page</li>
<li>13 - Bounced</li>
<li>14 - Spam Complaint</li>
<li>15 - Email Preference Page</li>
<li>16 - Resubscribed</li>
<li>17 - Click (Third Party)</li>
<li>18 - Opportunity Reopened</li>
<li>19 - Opportunity Linked</li>
<li>20 - Visit</li>
<li>21 - Custom URL click</li>
<li>22 - Olark Chat</li>
<li>23 - Invited to Webinar</li>
<li>24 - Attended Webinar</li>
<li>25 - Registered for Webinar</li>
<li>26 - Social Post Click</li>
<li>27 - Video View</li>
<li>28 - Event Registered</li>
<li>29 - Event Checked In</li>
<li>30 - Video Conversion</li>
<li>31 - UserVoice Suggestion</li>
<li>32 - UserVoice Comment</li>
<li>33 - UserVoice Ticket</li>
<li>34 - Video Watched (≥ 75% watched)</li>
<li>Other - Unknown</li>
</ul>
## Visitor Page View

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td></td>
<td></td>
<td>Pardot ID for this visitor page view</td>
</tr>
<tr>
<td>&lt;url&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Page view URL</td>
</tr>
<tr>
<td>&lt;title&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Page title</td>
</tr>
<tr>
<td>&lt;created_at&gt;</td>
<td>timestamp</td>
<td></td>
<td></td>
<td>Time page view occurred; Time is reported in API user's
preferred timezone</td>
</tr>
</table>
## Visitor Referrer

<table>
<tr>
<td><strong>Field Name&nbsp;</strong></td>
<td><strong>Data Type&nbsp;</strong></td>
<td><strong>Required&nbsp;</strong></td>
<td><strong>Editable&nbsp;</strong></td>
<td><strong>Description&nbsp;</strong></td>
</tr>
<tr>
<td>&lt;id&gt;</td>
<td>integer</td>
<td>X</td>
<td></td>
<td>Pardot ID for this visitor referrer</td>
</tr>
<tr>
<td>&lt;referrer&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Referrer's URL</td>
</tr>
<tr>
<td>&lt;vendor&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Referrer's vendor (such as 'Google' or 'Yahoo')</td>
</tr>
<tr>
<td>&lt;type&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Referrer's type (such as 'Natural Search')</td>
</tr>
<tr>
<td>&lt;query&gt;</td>
<td>string</td>
<td></td>
<td></td>
<td>Referrer's search query</td>
</tr>
</table>
