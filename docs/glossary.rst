Glossary
########

This section defines terms used throughout the :mod:`aioxmpp` documentation.

.. glossary::

   Conversation
     A context for communication between two or more :term:`entities <Entity>`.
     It defines a transport medium (such as direct XMPP or a Multi-User-Chat), a
     set of members along with their addresses and possibly additional features
     such as archive access method.

   Conversation Implementation
     A module consisting of service that implements
     :class:`aioxmpp.im.conversation.AbstractConversationService`
     together with implementations of
     :class:`aioxmpp.im.conversation.AbstractConversation` and
     :class:`aioxmpp.im.conversation.AbstractConversationMember`.
     This adds support for one concrete type of conversation to
     aioxmpp.  Currently, the following conversation implementations
     exist: :class:`aioxmpp.im.p2p` and :class:`aioxmpp.muc`.

   Conversation Member
     Representation of an :term:`entity <Entity>` which takes part in a
     :term:`conversation <Conversation>`. The actual definition of
     "taking part in a conversation" depends on the specific medium
     used. Conversation members are represented in aioxmpp as
     instances of
     :class:`aioxmpp.im.conversation.AbstractConversationMember`.

   Conversation Service
     A service implementing
     :class:`aioxmpp.im.conversation.AbstractConversationService`.
     This allows to create and manage :term:`conversations <Conversation>`.

   Entity
     An endpoint in the Jabber network, anything that can be addressed by
     a :term:`JID`. (Compare :rfc:`6122` section 2.1)

   Jabber ID
   JID
     Jabber Identifier. The unique address of an :term:`entity
     <Entity>` in the Jabber network. (Compare :rfc:`6122` section 2).

     Jabber IDs are represented as :class:`aioxmpp.JID` objects in aioxmpp.

   Tracking Service
     A :term:`Service` which provides functionality for updating
     :class:`aioxmpp.tracking.MessageTracker` objects.

   Service
     A subclass of :class:`aioxmpp.service.Service` which supplements the base
     :class:`aioxmpp.Client` with additional functionality. Typically, a
     service implements a part of one or more :term:`XEPs <XEP>`.

   Service Member
     A :term:`Conversation Member` representing the service over which the
     conversation is run. For example, some :xep:`45` multi-user chat
     service implementations send messages to all occupants as a service user.
     Those messages appear in :mod:`aioxmpp.muc` as coming from the service
     member.

     Relevant entities:

     * :attr:`aioxmpp.im.conversation.AbstractConversation.service_member`

        * :attr:`aioxmpp.muc.Room.service_member`

     * :class:`aioxmpp.im.conversation.AbstractConversationMember`

        * :attr:`aioxmpp.muc.ServiceMember`

   XEP
   XMPP Extension Proposal
     An XMPP Extension Proposal (or XEP) is a document which extends the basic
     RFCs of the XMPP protocol with additional functionality. Many important
     instant messaging features are specified in XEPs. The index of XEPs is
     located on `xmpp.org <https://xmpp.org/extensions/>`_.

   XSO
   XML stream object
     A XML stream object (or XSO) is a python representation of an XML subtree.
     Its name originates from the fact that it is mostly used with XMPP XML
     streams.

     The definition and use of XSOs is documented in :mod:`aioxmpp.xso`.
