Version: NAFATH-V2
Track: Software
## Overview
This project examines how six IT fields can help a telecom operator deliver a dependable 5G service for emergency responders. Software engineering supports safe request handling and reduces problems caused by repeated requests. Artificial Intelligence (AI) can predict possible network congestion and help the operator prepare in advance. Mobile development allows responders to access stored information and record updates without an active connection. Networking provides dedicated 5G resources to give emergency traffic higher priority. Cybersecurity helps detect attacks, limit their impact, and restore affected services. Data management organizes usage records so the operator can compare daily activity across regions. These fields work together to improve communication, support faster decisions, and reduce service disruptions. However, reliable emergency communication also requires careful testing, backup arrangements, and regular reviews to ensure the service remains useful during unexpected events.
## Software
HTTP methods have different purposes. GET and HEAD are safe because they retrieve information without requesting changes to the server. PUT and DELETE, along with safe methods, are idempotent, meaning repeated requests have the same intended effect as one request. POST is not idempotent by default and may create duplicate emergency reports if retried. Developers should therefore design retry rules carefully to avoid repeating important actions.

Resource: RFC 9110 - HTTP Semantics - https://www.rfc-editor.org/rfc/r9110.html

## AI
A congestion prediction model should perform well on both past records and new network conditions. Overfitting happens when the model learns the training examples too closely and fails to predict unfamiliar situations. Cross-validation helps check this by repeatedly training and evaluating the model on different parts of the available dataset. Comparing the results shows whether the model performs consistently or may struggle with new network data.

Resource: Scikit-learn - Cross-validation - https://scikit-learn.org/stable/modules/cross_validation.html

## Mobile
Emergency responders may enter areas where mobile connectivity is weak or unavailable. Their app should keep essential information on the device and allow important updates to be saved offline. It should clearly mark records waiting to be sent. Once the connection returns, the app should upload pending changes, retrieve updated information, and resolve conflicting edits. These steps help responders continue their work without losing important records during network outages.
Resource: Android Developers - Build on offline-first app - https://developer.android.com/topic/architecture/data-layer/offline-first
