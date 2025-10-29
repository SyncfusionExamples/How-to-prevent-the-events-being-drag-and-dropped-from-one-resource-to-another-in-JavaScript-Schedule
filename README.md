# How to prevent the events being drag and dropped from one resource to another in JavaScript Scheduler?

This example demonstrates how to restrict event drag-and-drop between different resources in the Syncfusion JavaScript Scheduler. The `dragStop` event is used to intercept and control the drag behavior.

Within the handler, we compare the groupIndex of the dragged event’s original element and the target element. If they differ, it means the user is attempting to move the event to a different resource group. To prevent this, we set `args.cancel = true`, which cancels the drag operation. This ensures that events remain assigned to their original resource (e.g., Alice or Smith) and cannot be moved across resource boundaries.

This approach is useful in scenarios where resource-specific scheduling must be preserved, such as team-based task assignments or equipment bookings. The Scheduler is configured with grouped resources, and each event is linked to an OwnerId, ensuring clear separation and control over scheduling responsibilities.