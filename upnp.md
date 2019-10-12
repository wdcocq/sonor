 urn:schemas-upnp-org:device:ZonePlayer:1
 - urn:schemas-upnp-org:service:AlarmClock:1
    SV: A_ARG_TYPE_ISO8601Time
    SV: A_ARG_TYPE_Recurrence
    SV: A_ARG_TYPE_AlarmID
    SV: A_ARG_TYPE_AlarmList
    SV: A_ARG_TYPE_AlarmEnabled
    SV: A_ARG_TYPE_AlarmProgramURI
    SV: A_ARG_TYPE_AlarmProgramMetaData
    SV: A_ARG_TYPE_AlarmPlayMode
    SV: A_ARG_TYPE_AlarmVolume
    SV: A_ARG_TYPE_AlarmIncludeLinkedZones
    SV: A_ARG_TYPE_AlarmRoomUUID
    SV: A_ARG_TYPE_TimeZoneIndex
    SV: A_ARG_TYPE_TimeZoneAutoAdjustDst
    SV: A_ARG_TYPE_TimeZoneInformation
    SV: A_ARG_TYPE_TimeStamp
    SV: TimeZone
    SV: TimeServer
    SV: TimeGeneration
    SV: AlarmListVersion
    SV: DailyIndexRefreshTime
    SV: TimeFormat
    SV: DateFormat
    AC: SetFormat(DesiredTimeFormat: String, DesiredDateFormat: String)
    AC: GetFormat() -> (CurrentTimeFormat: String, CurrentDateFormat: String)
    AC: SetTimeZone(Index: i4, AutoAdjustDst: Boolean)
    AC: GetTimeZone() -> (Index: i4, AutoAdjustDst: Boolean)
    AC: GetTimeZoneAndRule() -> (Index: i4, AutoAdjustDst: Boolean, CurrentTimeZone: String)
    AC: GetTimeZoneRule(Index: i4) -> (TimeZone: String)
    AC: SetTimeServer(DesiredTimeServer: String)
    AC: GetTimeServer() -> (CurrentTimeServer: String)
    AC: SetTimeNow(DesiredTime: String, TimeZoneForDesiredTime: String)
    AC: GetHouseholdTimeAtStamp(TimeStamp: String) -> (HouseholdUTCTime: String)
    AC: GetTimeNow() -> (CurrentUTCTime: String, CurrentLocalTime: String, CurrentTimeZone: String, CurrentTimeGeneration: ui4)
    AC: CreateAlarm(StartLocalTime: String, Duration: String, Recurrence: [ONCE, WEEKDAYS, WEEKENDS, DAILY], Enabled: Boolean, RoomUUID: String, ProgramURI: String, ProgramMetaData: String, PlayMode: [NORMAL, REPEAT_ALL, SHUFFLE_NOREPEAT, SHUFFLE] = NORMAL, Volume: ui2, IncludeLinkedZones: Boolean) -> (AssignedID: ui4)
    AC: UpdateAlarm(ID: ui4, StartLocalTime: String, Duration: String, Recurrence: [ONCE, WEEKDAYS, WEEKENDS, DAILY], Enabled: Boolean, RoomUUID: String, ProgramURI: String, ProgramMetaData: String, PlayMode: [NORMAL, REPEAT_ALL, SHUFFLE_NOREPEAT, SHUFFLE] = NORMAL, Volume: ui2, IncludeLinkedZones: Boolean)
    AC: DestroyAlarm(ID: ui4)
    AC: ListAlarms() -> (CurrentAlarmList: String, CurrentAlarmListVersion: String)
    AC: SetDailyIndexRefreshTime(DesiredDailyIndexRefreshTime: String)
    AC: GetDailyIndexRefreshTime() -> (CurrentDailyIndexRefreshTime: String)
 - urn:schemas-upnp-org:service:MusicServices:1
    SV: A_ARG_TYPE_ServiceDescriptorList
    SV: A_ARG_TYPE_ServiceTypeList
    SV: ServiceId
    SV: ServiceListVersion
    SV: SessionId
    SV: Username
    AC: GetSessionId(ServiceId: ui4, Username: String) -> (SessionId: String)
    AC: ListAvailableServices() -> (AvailableServiceDescriptorList: String, AvailableServiceTypeList: String, AvailableServiceListVersion: String)
    AC: UpdateAvailableServices()
 - urn:schemas-upnp-org:service:AudioIn:1
    SV: A_ARG_TYPE_MemberID
    SV: A_ARG_TYPE_TransportSettings
    SV: AudioInputName
    SV: Icon
    SV: LineInConnected
    SV: LeftLineInLevel
    SV: RightLineInLevel
    SV: A_ARG_TYPE_ObjectID
    SV: Playing
    AC: StartTransmissionToGroup(CoordinatorID: String) -> (CurrentTransportSettings: String)
    AC: StopTransmissionToGroup(CoordinatorID: String)
    AC: SetAudioInputAttributes(DesiredName: String, DesiredIcon: String)
    AC: GetAudioInputAttributes() -> (CurrentName: String, CurrentIcon: String)
    AC: SetLineInLevel(DesiredLeftLineInLevel: i4, DesiredRightLineInLevel: i4)
    AC: GetLineInLevel() -> (CurrentLeftLineInLevel: i4, CurrentRightLineInLevel: i4)
    AC: SelectAudio(ObjectID: String)
 - urn:schemas-upnp-org:service:DeviceProperties:1
    SV: HouseholdID
    SV: SettingsReplicationState
    SV: ZoneName
    SV: Icon
    SV: Configuration
    SV: Invisible
    SV: IsZoneBridge
    SV: AirPlayEnabled
    SV: SupportsAudioIn
    SV: SupportsAudioClip
    SV: IsIdle
    SV: MoreInfo
    SV: ChannelMapSet
    SV: HTSatChanMapSet
    SV: HTFreq
    SV: HTBondedZoneCommitState
    SV: Orientation
    SV: LastChangedPlayState
    SV: RoomCalibrationState
    SV: AvailableRoomCalibration
    SV: SatRoomUUID
    SV: LEDState
    SV: SerialNumber
    SV: SoftwareVersion
    SV: DisplaySoftwareVersion
    SV: HardwareVersion
    SV: IPAddress
    SV: MACAddress
    SV: CopyrightInfo
    SV: ExtraInfo
    SV: HTAudioIn
    SV: Flags
    SV: AutoplayIncludeLinkedZones
    SV: AutoplayRoomUUID
    SV: AutoplaySource
    SV: AutoplayVolume
    SV: AutoplayUseVolume
    SV: TVConfigurationError
    SV: HdmiCecAvailable
    SV: WirelessMode
    SV: WirelessLeafOnly
    SV: HasConfiguredSSID
    SV: ChannelFreq
    SV: BehindWifiExtender
    SV: WifiEnabled
    SV: ConfigMode
    SV: SecureRegState
    SV: A_ARG_TYPE_ConfigModeOptions
    SV: A_ARG_TYPE_ConfigModeState
    SV: A_ARG_TYPE_ButtonState
    SV: ButtonLockState
    SV: VoiceConfigState
    SV: MicEnabled
    SV: KeepGrouped
    AC: SetLEDState(DesiredLEDState: [On, Off])
    AC: GetLEDState() -> (CurrentLEDState: [On, Off])
    AC: AddBondedZones(ChannelMapSet: String)
    AC: RemoveBondedZones(ChannelMapSet: String, KeepGrouped: Boolean)
    AC: CreateStereoPair(ChannelMapSet: String)
    AC: SeparateStereoPair(ChannelMapSet: String)
    AC: SetZoneAttributes(DesiredZoneName: String, DesiredIcon: String, DesiredConfiguration: String)
    AC: GetZoneAttributes() -> (CurrentZoneName: String, CurrentIcon: String, CurrentConfiguration: String)
    AC: GetHouseholdID() -> (CurrentHouseholdID: String)
    AC: GetZoneInfo() -> (SerialNumber: String, SoftwareVersion: String, DisplaySoftwareVersion: String, HardwareVersion: String, IPAddress: String, MACAddress: String, CopyrightInfo: String, ExtraInfo: String, HTAudioIn: ui4, Flags: ui4)
    AC: SetAutoplayLinkedZones(IncludeLinkedZones: Boolean, Source: String)
    AC: GetAutoplayLinkedZones(Source: String) -> (IncludeLinkedZones: Boolean)
    AC: SetAutoplayRoomUUID(RoomUUID: String, Source: String)
    AC: GetAutoplayRoomUUID(Source: String) -> (RoomUUID: String)
    AC: SetAutoplayVolume(Volume: ui2, Source: String)
    AC: GetAutoplayVolume(Source: String) -> (CurrentVolume: ui2)
    AC: SetUseAutoplayVolume(UseVolume: Boolean, Source: String)
    AC: GetUseAutoplayVolume(Source: String) -> (UseVolume: Boolean)
    AC: AddHTSatellite(HTSatChanMapSet: String)
    AC: RemoveHTSatellite(SatRoomUUID: String)
    AC: EnterConfigMode(Mode: String, Options: String) -> (State: String)
    AC: ExitConfigMode(Options: String)
    AC: GetButtonState() -> (State: String)
    AC: SetButtonLockState(DesiredButtonLockState: [On, Off])
    AC: GetButtonLockState() -> (CurrentButtonLockState: [On, Off])
 - urn:schemas-upnp-org:service:SystemProperties:1
    SV: A_ARG_TYPE_VariableName
    SV: A_ARG_TYPE_VariableStringValue
    SV: A_ARG_TYPE_AccountType
    SV: A_ARG_TYPE_AccountUID
    SV: A_ARG_TYPE_AccountUDN
    SV: A_ARG_TYPE_AccountID
    SV: A_ARG_TYPE_AccountPassword
    SV: A_ARG_TYPE_AccountNickname
    SV: A_ARG_TYPE_AccountCredential
    SV: A_ARG_TYPE_AccountMd
    SV: A_ARG_TYPE_IsExpired
    SV: A_ARG_TYPE_StubsCreated
    SV: A_ARG_TYPE_RDMEnabled
    SV: A_ARG_TYPE_OAuthDeviceID
    SV: A_ARG_TYPE_AuthorizationCode
    SV: A_ARG_TYPE_UserIdHashCode
    SV: A_ARG_TYPE_AccountTier
    SV: A_ARG_TYPE_RedirectURI
    SV: CustomerID
    SV: UpdateID
    SV: UpdateIDX
    SV: VoiceUpdateID
    SV: ThirdPartyHash
    AC: SetString(VariableName: String, StringValue: String)
    AC: GetString(VariableName: String) -> (StringValue: String)
    AC: Remove(VariableName: String)
    AC: GetWebCode(AccountType: ui4) -> (WebCode: String)
    AC: ProvisionCredentialedTrialAccountX(AccountType: ui4, AccountID: String, AccountPassword: String) -> (IsExpired: Boolean, AccountUDN: String)
    AC: AddAccountX(AccountType: ui4, AccountID: String, AccountPassword: String) -> (AccountUDN: String)
    AC: AddOAuthAccountX(AccountType: ui4, AccountToken: String, AccountKey: String, OAuthDeviceID: String, AuthorizationCode: String, RedirectURI: String, UserIdHashCode: String, AccountTier: ui4) -> (AccountUDN: String, AccountNickname: String)
    AC: RemoveAccount(AccountType: ui4, AccountID: String)
    AC: EditAccountPasswordX(AccountType: ui4, AccountID: String, NewAccountPassword: String)
    AC: SetAccountNicknameX(AccountUDN: String, AccountNickname: String)
    AC: RefreshAccountCredentialsX(AccountType: ui4, AccountUID: ui4, AccountToken: String, AccountKey: String)
    AC: EditAccountMd(AccountType: ui4, AccountID: String, NewAccountMd: String)
    AC: DoPostUpdateTasks()
    AC: ResetThirdPartyCredentials()
    AC: EnableRDM(RDMValue: Boolean)
    AC: GetRDM() -> (RDMValue: Boolean)
    AC: ReplaceAccountX(AccountUDN: String, NewAccountID: String, NewAccountPassword: String, AccountToken: String, AccountKey: String, OAuthDeviceID: String) -> (NewAccountUDN: String)
 - urn:schemas-upnp-org:service:ZoneGroupTopology:1
    SV: AvailableSoftwareUpdate
    SV: ZoneGroupState
    SV: ThirdPartyMediaServersX
    SV: AlarmRunSequence
    SV: MuseHouseholdId
    SV: ZoneGroupName
    SV: ZoneGroupID
    SV: ZonePlayerUUIDsInGroup
    SV: A_ARG_TYPE_UpdateType
    SV: A_ARG_TYPE_CachedOnly
    SV: A_ARG_TYPE_UpdateItem
    SV: A_ARG_TYPE_UpdateURL
    SV: A_ARG_TYPE_UpdateFlags
    SV: A_ARG_TYPE_UpdateExtraOptions
    SV: A_ARG_TYPE_Version
    SV: A_ARG_TYPE_MemberID
    SV: A_ARG_TYPE_UnresponsiveDeviceActionType
    SV: DiagnosticID
    SV: A_ARG_TYPE_IncludeControllers
    SV: A_ARG_TYPE_Origin
    SV: A_ARG_TYPE_MobileDeviceName
    SV: A_ARG_TYPE_MobileDeviceUDN
    SV: A_ARG_TYPE_MobileIPAndPort
    SV: AreasUpdateID
    SV: SourceAreasUpdateID
    SV: NetsettingsUpdateID
    AC: CheckForUpdate(UpdateType: [All, Software], CachedOnly: Boolean, Version: String) -> (UpdateItem: String)
    AC: BeginSoftwareUpdate(UpdateURL: String, Flags: ui4, ExtraOptions: String)
    AC: ReportUnresponsiveDevice(DeviceUUID: String, DesiredAction: [Remove, TopologyMonitorProbe, VerifyThenRemoveSystemwide])
    AC: ReportAlarmStartedRunning()
    AC: SubmitDiagnostics(IncludeControllers: Boolean, Type: String) -> (DiagnosticID: ui4)
    AC: RegisterMobileDevice(MobileDeviceName: String, MobileDeviceUDN: String, MobileIPAndPort: String)
    AC: GetZoneGroupAttributes() -> (CurrentZoneGroupName: String, CurrentZoneGroupID: String, CurrentZonePlayerUUIDsInGroup: String, CurrentMuseHouseholdId: String)
    AC: GetZoneGroupState() -> (ZoneGroupState: String)
 - urn:schemas-upnp-org:service:GroupManagement:1
    SV: A_ARG_TYPE_MemberID
    SV: A_ARG_TYPE_TransportSettings
    SV: A_ARG_TYPE_AVTransportURI
    SV: A_ARG_TYPE_BufferingResultCode
    SV: A_ARG_TYPE_BootSeq
    SV: GroupCoordinatorIsLocal
    SV: LocalGroupUUID
    SV: VirtualLineInGroupID
    SV: SourceAreaIds
    SV: ResetVolumeAfter
    SV: VolumeAVTransportURI
    AC: AddMember(MemberID: String, BootSeq: ui4) -> (CurrentTransportSettings: String, CurrentURI: String, GroupUUIDJoined: String, ResetVolumeAfter: Boolean, VolumeAVTransportURI: String)
    AC: RemoveMember(MemberID: String)
    AC: ReportTrackBufferingResult(MemberID: String, ResultCode: i4)
    AC: SetSourceAreaIds(DesiredSourceAreaIds: String)
 - urn:schemas-tencent-com:service:QPlay:1
    SV: A_ARG_TYPE_Seed
    SV: A_ARG_TYPE_Code
    SV: A_ARG_TYPE_MID
    SV: A_ARG_TYPE_DID
    AC: QPlayAuth(Seed: String) -> (Code: String, MID: String, DID: String)
   urn:schemas-upnp-org:device:MediaServer:1
   - urn:schemas-upnp-org:service:ContentDirectory:1
      SV: A_ARG_TYPE_ObjectID
      SV: A_ARG_TYPE_Result
      SV: A_ARG_TYPE_SearchCriteria
      SV: A_ARG_TYPE_BrowseFlag
      SV: A_ARG_TYPE_Filter
      SV: A_ARG_TYPE_SortCriteria
      SV: A_ARG_TYPE_Prefix
      SV: A_ARG_TYPE_Index
      SV: A_ARG_TYPE_Count
      SV: A_ARG_TYPE_UpdateID
      SV: A_ARG_TYPE_TagValueList
      SV: A_ARG_TYPE_AlbumArtistDisplayOption
      SV: A_ARG_TYPE_SortOrder
      SV: A_ARG_TYPE_LastIndexChange
      SV: SearchCapabilities
      SV: SortCapabilities
      SV: SystemUpdateID
      SV: ContainerUpdateIDs
      SV: ShareIndexInProgress
      SV: ShareIndexLastError
      SV: UserRadioUpdateID
      SV: SavedQueuesUpdateID
      SV: ShareListUpdateID
      SV: RecentlyPlayedUpdateID
      SV: Browseable
      SV: RadioFavoritesUpdateID
      SV: RadioLocationUpdateID
      SV: FavoritesUpdateID
      SV: FavoritePresetsUpdateID
      AC: GetSearchCapabilities() -> (SearchCaps: String)
      AC: GetSortCapabilities() -> (SortCaps: String)
      AC: GetSystemUpdateID() -> (Id: ui4)
      AC: GetAlbumArtistDisplayOption() -> (AlbumArtistDisplayOption: String)
      AC: GetLastIndexChange() -> (LastIndexChange: String)
      AC: Browse(ObjectID: String, BrowseFlag: [BrowseMetadata, BrowseDirectChildren], Filter: String, StartingIndex: ui4, RequestedCount: ui4, SortCriteria: String) -> (Result: String, NumberReturned: ui4, TotalMatches: ui4, UpdateID: ui4)
      AC: FindPrefix(ObjectID: String, Prefix: String) -> (StartingIndex: ui4, UpdateID: ui4)
      AC: GetAllPrefixLocations(ObjectID: String) -> (TotalPrefixes: ui4, PrefixAndIndexCSV: String, UpdateID: ui4)
      AC: CreateObject(ContainerID: String, Elements: String) -> (ObjectID: String, Result: String)
      AC: UpdateObject(ObjectID: String, CurrentTagValue: String, NewTagValue: String)
      AC: DestroyObject(ObjectID: String)
      AC: RefreshShareIndex(AlbumArtistDisplayOption: String)
      AC: RequestResort(SortOrder: String)
      AC: GetShareIndexInProgress() -> (IsIndexing: Boolean)
      AC: GetBrowseable() -> (IsBrowseable: Boolean)
      AC: SetBrowseable(Browseable: Boolean)
   - urn:schemas-upnp-org:service:ConnectionManager:1
      SV: SourceProtocolInfo
      SV: SinkProtocolInfo
      SV: CurrentConnectionIDs
      SV: A_ARG_TYPE_ConnectionStatus
      SV: A_ARG_TYPE_ConnectionManager
      SV: A_ARG_TYPE_Direction
      SV: A_ARG_TYPE_ProtocolInfo
      SV: A_ARG_TYPE_ConnectionID
      SV: A_ARG_TYPE_AVTransportID
      SV: A_ARG_TYPE_RcsID
      AC: GetProtocolInfo() -> (Source: String, Sink: String)
      AC: GetCurrentConnectionIDs() -> (ConnectionIDs: String)
      AC: GetCurrentConnectionInfo(ConnectionID: i4) -> (RcsID: i4, AVTransportID: i4, ProtocolInfo: String, PeerConnectionManager: String, PeerConnectionID: i4, Direction: [Input, Output], Status: [OK, ContentFormatMismatch, InsufficientBandwidth, UnreliableChannel, Unknown])
   urn:schemas-upnp-org:device:MediaRenderer:1
   - urn:schemas-upnp-org:service:RenderingControl:1
      SV: LastChange
      SV: Mute
      SV: Volume
      SV: A_ARG_TYPE_LeftVolume
      SV: A_ARG_TYPE_RightVolume
      SV: VolumeDB
      SV: Bass
      SV: Treble
      SV: EQValue
      SV: A_ARG_TYPE_EQType
      SV: Loudness
      SV: SupportsOutputFixed
      SV: OutputFixed
      SV: HeadphoneConnected
      SV: A_ARG_TYPE_Channel
      SV: A_ARG_TYPE_MuteChannel
      SV: A_ARG_TYPE_InstanceID
      SV: A_ARG_TYPE_VolumeAdjustment
      SV: A_ARG_TYPE_RampType
      SV: A_ARG_TYPE_RampTimeSeconds
      SV: A_ARG_TYPE_ResetVolumeAfter
      SV: A_ARG_TYPE_ProgramURI
      SV: A_ARG_TYPE_ChannelMap
      SV: AudioDelay
      SV: AudioDelayLeftRear
      SV: AudioDelayRightRear
      SV: DialogLevel
      SV: SpeakerSize
      SV: SubCrossover
      SV: SubEnabled
      SV: SubGain
      SV: SubPolarity
      SV: SurroundLevel
      SV: MusicSurroundLevel
      SV: NightMode
      SV: SurroundEnabled
      SV: SurroundMode
      SV: PresetNameList
      SV: RoomCalibrationID
      SV: RoomCalibrationCoefficients
      SV: RoomCalibrationCalibrationMode
      SV: RoomCalibrationEnabled
      SV: RoomCalibrationAvailable
      AC: GetMute(InstanceID: ui4, Channel: [Master, LF, RF, SpeakerOnly]) -> (CurrentMute: Boolean)
      AC: SetMute(InstanceID: ui4, Channel: [Master, LF, RF, SpeakerOnly], DesiredMute: Boolean)
      AC: ResetBasicEQ(InstanceID: ui4) -> (Bass: i2, Treble: i2, Loudness: Boolean, LeftVolume: ui2, RightVolume: ui2)
      AC: ResetExtEQ(InstanceID: ui4, EQType: String)
      AC: GetVolume(InstanceID: ui4, Channel: [Master, LF, RF]) -> (CurrentVolume: ui2)
      AC: SetVolume(InstanceID: ui4, Channel: [Master, LF, RF], DesiredVolume: ui2)
      AC: SetRelativeVolume(InstanceID: ui4, Channel: [Master, LF, RF], Adjustment: i4) -> (NewVolume: ui2)
      AC: GetVolumeDB(InstanceID: ui4, Channel: [Master, LF, RF]) -> (CurrentVolume: i2)
      AC: SetVolumeDB(InstanceID: ui4, Channel: [Master, LF, RF], DesiredVolume: i2)
      AC: GetVolumeDBRange(InstanceID: ui4, Channel: [Master, LF, RF]) -> (MinValue: i2, MaxValue: i2)
      AC: GetBass(InstanceID: ui4) -> (CurrentBass: i2)
      AC: SetBass(InstanceID: ui4, DesiredBass: i2)
      AC: GetTreble(InstanceID: ui4) -> (CurrentTreble: i2)
      AC: SetTreble(InstanceID: ui4, DesiredTreble: i2)
      AC: GetEQ(InstanceID: ui4, EQType: String) -> (CurrentValue: i2)
      AC: SetEQ(InstanceID: ui4, EQType: String, DesiredValue: i2)
      AC: GetLoudness(InstanceID: ui4, Channel: [Master, LF, RF]) -> (CurrentLoudness: Boolean)
      AC: SetLoudness(InstanceID: ui4, Channel: [Master, LF, RF], DesiredLoudness: Boolean)
      AC: GetSupportsOutputFixed(InstanceID: ui4) -> (CurrentSupportsFixed: Boolean)
      AC: GetOutputFixed(InstanceID: ui4) -> (CurrentFixed: Boolean)
      AC: SetOutputFixed(InstanceID: ui4, DesiredFixed: Boolean)
      AC: GetHeadphoneConnected(InstanceID: ui4) -> (CurrentHeadphoneConnected: Boolean)
      AC: RampToVolume(InstanceID: ui4, Channel: [Master, LF, RF], RampType: [SLEEP_TIMER_RAMP_TYPE, ALARM_RAMP_TYPE, AUTOPLAY_RAMP_TYPE], DesiredVolume: ui2, ResetVolumeAfter: Boolean, ProgramURI: String) -> (RampTime: ui4)
      AC: RestoreVolumePriorToRamp(InstanceID: ui4, Channel: [Master, LF, RF])
      AC: SetChannelMap(InstanceID: ui4, ChannelMap: String)
      AC: SetRoomCalibrationX(InstanceID: ui4, CalibrationID: String, Coefficients: String, CalibrationMode: String)
      AC: GetRoomCalibrationStatus(InstanceID: ui4) -> (RoomCalibrationEnabled: Boolean, RoomCalibrationAvailable: Boolean)
      AC: SetRoomCalibrationStatus(InstanceID: ui4, RoomCalibrationEnabled: Boolean)
   - urn:schemas-upnp-org:service:ConnectionManager:1
      SV: SourceProtocolInfo
      SV: SinkProtocolInfo
      SV: CurrentConnectionIDs
      SV: A_ARG_TYPE_ConnectionStatus
      SV: A_ARG_TYPE_ConnectionManager
      SV: A_ARG_TYPE_Direction
      SV: A_ARG_TYPE_ProtocolInfo
      SV: A_ARG_TYPE_ConnectionID
      SV: A_ARG_TYPE_AVTransportID
      SV: A_ARG_TYPE_RcsID
      AC: GetProtocolInfo() -> (Source: String, Sink: String)
      AC: GetCurrentConnectionIDs() -> (ConnectionIDs: String)
      AC: GetCurrentConnectionInfo(ConnectionID: i4) -> (RcsID: i4, AVTransportID: i4, ProtocolInfo: String, PeerConnectionManager: String, PeerConnectionID: i4, Direction: [Input, Output], Status: [OK, ContentFormatMismatch, InsufficientBandwidth, UnreliableChannel, Unknown])
   - urn:schemas-upnp-org:service:AVTransport:1
      SV: TransportState
      SV: TransportStatus
      SV: TransportErrorDescription
      SV: TransportErrorURI
      SV: TransportErrorHttpCode
      SV: TransportErrorHttpHeaders
      SV: PlaybackStorageMedium
      SV: RecordStorageMedium
      SV: PossiblePlaybackStorageMedia
      SV: PossibleRecordStorageMedia
      SV: CurrentPlayMode
      SV: CurrentCrossfadeMode
      SV: TransportPlaySpeed
      SV: RecordMediumWriteStatus
      SV: CurrentRecordQualityMode
      SV: PossibleRecordQualityModes
      SV: NumberOfTracks
      SV: CurrentTrack
      SV: CurrentSection
      SV: CurrentTrackDuration
      SV: CurrentMediaDuration
      SV: CurrentTrackMetaData
      SV: CurrentTrackURI
      SV: AVTransportURI
      SV: AVTransportURIMetaData
      SV: NextAVTransportURI
      SV: NextAVTransportURIMetaData
      SV: RelativeTimePosition
      SV: AbsoluteTimePosition
      SV: RelativeCounterPosition
      SV: AbsoluteCounterPosition
      SV: CurrentTransportActions
      SV: SleepTimerGeneration
      SV: SnoozeRunning
      SV: AlarmRunning
      SV: AlarmIDRunning
      SV: AlarmLoggedStartTime
      SV: RestartPending
      SV: LastChange
      SV: NextTrackMetaData
      SV: NextTrackURI
      SV: EnqueuedTransportURIMetaData
      SV: EnqueuedTransportURI
      SV: CurrentValidPlayModes
      SV: MuseSessions
      SV: DirectControlClientID
      SV: DirectControlAccountID
      SV: DirectControlIsSuspended
      SV: A_ARG_TYPE_SeekMode
      SV: A_ARG_TYPE_SeekTarget
      SV: A_ARG_TYPE_InstanceID
      SV: A_ARG_TYPE_MemberList
      SV: A_ARG_TYPE_TransportSettings
      SV: A_ARG_TYPE_CurrentAVTransportURI
      SV: A_ARG_TYPE_SourceState
      SV: A_ARG_TYPE_VLIState
      SV: A_ARG_TYPE_Queue
      SV: A_ARG_TYPE_MemberID
      SV: A_ARG_TYPE_URI
      SV: A_ARG_TYPE_LIST_URI
      SV: A_ARG_TYPE_URIMetaData
      SV: A_ARG_TYPE_LIST_URIMetaData
      SV: A_ARG_TYPE_ObjectID
      SV: A_ARG_TYPE_GroupID
      SV: A_ARG_TYPE_PlayerID
      SV: A_ARG_TYPE_TrackNumber
      SV: A_ARG_TYPE_NumTracks
      SV: A_ARG_TYPE_NumTracksChange
      SV: A_ARG_TYPE_EnqueueAsNext
      SV: A_ARG_TYPE_SavedQueueTitle
      SV: A_ARG_TYPE_ResumePlayback
      SV: A_ARG_TYPE_ISO8601Time
      SV: A_ARG_TYPE_AlarmVolume
      SV: A_ARG_TYPE_AlarmIncludeLinkedZones
      SV: A_ARG_TYPE_ResetVolumeAfter
      SV: A_ARG_TYPE_SleepTimerState
      SV: A_ARG_TYPE_AlarmState
      SV: A_ARG_TYPE_StreamRestartState
      SV: A_ARG_TYPE_RejoinGroup
      SV: QueueUpdateID
      SV: A_ARG_TYPE_TrackList
      AC: SetAVTransportURI(InstanceID: ui4, CurrentURI: String, CurrentURIMetaData: String)
      AC: SetNextAVTransportURI(InstanceID: ui4, NextURI: String, NextURIMetaData: String)
      AC: AddURIToQueue(InstanceID: ui4, EnqueuedURI: String, EnqueuedURIMetaData: String, DesiredFirstTrackNumberEnqueued: ui4, EnqueueAsNext: Boolean) -> (FirstTrackNumberEnqueued: ui4, NumTracksAdded: ui4, NewQueueLength: ui4)
      AC: AddMultipleURIsToQueue(InstanceID: ui4, UpdateID: ui4, NumberOfURIs: ui4, EnqueuedURIs: String, EnqueuedURIsMetaData: String, ContainerURI: String, ContainerMetaData: String, DesiredFirstTrackNumberEnqueued: ui4, EnqueueAsNext: Boolean) -> (FirstTrackNumberEnqueued: ui4, NumTracksAdded: ui4, NewQueueLength: ui4, NewUpdateID: ui4)
      AC: ReorderTracksInQueue(InstanceID: ui4, StartingIndex: ui4, NumberOfTracks: ui4, InsertBefore: ui4, UpdateID: ui4)
      AC: RemoveTrackFromQueue(InstanceID: ui4, ObjectID: String, UpdateID: ui4)
      AC: RemoveTrackRangeFromQueue(InstanceID: ui4, UpdateID: ui4, StartingIndex: ui4, NumberOfTracks: ui4) -> (NewUpdateID: ui4)
      AC: RemoveAllTracksFromQueue(InstanceID: ui4)
      AC: SaveQueue(InstanceID: ui4, Title: String, ObjectID: String) -> (AssignedObjectID: String)
      AC: BackupQueue(InstanceID: ui4)
      AC: CreateSavedQueue(InstanceID: ui4, Title: String, EnqueuedURI: String, EnqueuedURIMetaData: String) -> (NumTracksAdded: ui4, NewQueueLength: ui4, AssignedObjectID: String, NewUpdateID: ui4)
      AC: AddURIToSavedQueue(InstanceID: ui4, ObjectID: String, UpdateID: ui4, EnqueuedURI: String, EnqueuedURIMetaData: String, AddAtIndex: ui4) -> (NumTracksAdded: ui4, NewQueueLength: ui4, NewUpdateID: ui4)
      AC: ReorderTracksInSavedQueue(InstanceID: ui4, ObjectID: String, UpdateID: ui4, TrackList: String, NewPositionList: String) -> (QueueLengthChange: i4, NewQueueLength: ui4, NewUpdateID: ui4)
      AC: GetMediaInfo(InstanceID: ui4) -> (NrTracks: ui4, MediaDuration: String, CurrentURI: String, CurrentURIMetaData: String, NextURI: String, NextURIMetaData: String, PlayMedium: [NONE, NETWORK], RecordMedium: [NONE], WriteStatus: String)
      AC: GetTransportInfo(InstanceID: ui4) -> (CurrentTransportState: [STOPPED, PLAYING, PAUSED_PLAYBACK, TRANSITIONING], CurrentTransportStatus: String, CurrentSpeed: [1])
      AC: GetPositionInfo(InstanceID: ui4) -> (Track: ui4, TrackDuration: String, TrackMetaData: String, TrackURI: String, RelTime: String, AbsTime: String, RelCount: i4, AbsCount: i4)
      AC: GetDeviceCapabilities(InstanceID: ui4) -> (PlayMedia: String, RecMedia: String, RecQualityModes: String)
      AC: GetTransportSettings(InstanceID: ui4) -> (PlayMode: [NORMAL, REPEAT_ALL, REPEAT_ONE, SHUFFLE_NOREPEAT, SHUFFLE, SHUFFLE_REPEAT_ONE] = NORMAL, RecQualityMode: String)
      AC: GetCrossfadeMode(InstanceID: ui4) -> (CrossfadeMode: Boolean)
      AC: Stop(InstanceID: ui4)
      AC: Play(InstanceID: ui4, Speed: [1])
      AC: Pause(InstanceID: ui4)
      AC: Seek(InstanceID: ui4, Unit: [TRACK_NR, REL_TIME, TIME_DELTA], Target: String)
      AC: Next(InstanceID: ui4)
      AC: Previous(InstanceID: ui4)
      AC: SetPlayMode(InstanceID: ui4, NewPlayMode: [NORMAL, REPEAT_ALL, REPEAT_ONE, SHUFFLE_NOREPEAT, SHUFFLE, SHUFFLE_REPEAT_ONE] = NORMAL)
      AC: SetCrossfadeMode(InstanceID: ui4, CrossfadeMode: Boolean)
      AC: NotifyDeletedURI(InstanceID: ui4, DeletedURI: String)
      AC: GetCurrentTransportActions(InstanceID: ui4) -> (Actions: String)
      AC: BecomeCoordinatorOfStandaloneGroup(InstanceID: ui4) -> (DelegatedGroupCoordinatorID: String, NewGroupID: String)
      AC: DelegateGroupCoordinationTo(InstanceID: ui4, NewCoordinator: String, RejoinGroup: Boolean)
      AC: BecomeGroupCoordinator(InstanceID: ui4, CurrentCoordinator: String, CurrentGroupID: String, OtherMembers: String, TransportSettings: String, CurrentURI: String, CurrentURIMetaData: String, SleepTimerState: String, AlarmState: String, StreamRestartState: String, CurrentQueueTrackList: String, CurrentVLIState: String)
      AC: BecomeGroupCoordinatorAndSource(InstanceID: ui4, CurrentCoordinator: String, CurrentGroupID: String, OtherMembers: String, CurrentURI: String, CurrentURIMetaData: String, SleepTimerState: String, AlarmState: String, StreamRestartState: String, CurrentAVTTrackList: String, CurrentQueueTrackList: String, CurrentSourceState: String, ResumePlayback: Boolean)
      AC: ChangeCoordinator(InstanceID: ui4, CurrentCoordinator: String, NewCoordinator: String, NewTransportSettings: String, CurrentAVTransportURI: String)
      AC: ChangeTransportSettings(InstanceID: ui4, NewTransportSettings: String, CurrentAVTransportURI: String)
      AC: ConfigureSleepTimer(InstanceID: ui4, NewSleepTimerDuration: String)
      AC: GetRemainingSleepTimerDuration(InstanceID: ui4) -> (RemainingSleepTimerDuration: String, CurrentSleepTimerGeneration: ui4)
      AC: RunAlarm(InstanceID: ui4, AlarmID: ui4, LoggedStartTime: String, Duration: String, ProgramURI: String, ProgramMetaData: String, PlayMode: [NORMAL, REPEAT_ALL, REPEAT_ONE, SHUFFLE_NOREPEAT, SHUFFLE, SHUFFLE_REPEAT_ONE] = NORMAL, Volume: ui2, IncludeLinkedZones: Boolean)
      AC: StartAutoplay(InstanceID: ui4, ProgramURI: String, ProgramMetaData: String, Volume: ui2, IncludeLinkedZones: Boolean, ResetVolumeAfter: Boolean)
      AC: GetRunningAlarmProperties(InstanceID: ui4) -> (AlarmID: ui4, GroupID: String, LoggedStartTime: String)
      AC: SnoozeAlarm(InstanceID: ui4, Duration: String)
      AC: EndDirectControlSession(InstanceID: ui4)
   - urn:schemas-sonos-com:service:Queue:1
      SV: LastChange
      SV: UpdateID
      SV: Curated
      SV: A_ARG_TYPE_UpdateID
      SV: A_ARG_TYPE_QueueID
      SV: A_ARG_TYPE_QueueOwnerID
      SV: A_ARG_TYPE_QueueOwnerContext
      SV: A_ARG_TYPE_QueuePolicy
      SV: A_ARG_TYPE_URI
      SV: A_ARG_TYPE_LIST_URI
      SV: A_ARG_TYPE_URIMetaData
      SV: A_ARG_TYPE_ObjectID
      SV: A_ARG_TYPE_TrackNumber
      SV: A_ARG_TYPE_NumTracks
      SV: A_ARG_TYPE_EnqueueAsNext
      SV: A_ARG_TYPE_SavedQueueTitle
      SV: A_ARG_TYPE_Index
      SV: A_ARG_TYPE_Count
      SV: A_ARG_TYPE_Result
      SV: A_ARG_TYPE_SavedQueueTitle
      SV: A_ARG_TYPE_TrackNumbersCSV
      SV: A_ARG_TYPE_LIST_URI_AND_METADATA
      AC: AddURI(QueueID: ui4, UpdateID: ui4, EnqueuedURI: String, EnqueuedURIMetaData: String, DesiredFirstTrackNumberEnqueued: ui4, EnqueueAsNext: Boolean) -> (FirstTrackNumberEnqueued: ui4, NumTracksAdded: ui4, NewQueueLength: ui4, NewUpdateID: ui4)
      AC: AddMultipleURIs(QueueID: ui4, UpdateID: ui4, ContainerURI: String, ContainerMetaData: String, DesiredFirstTrackNumberEnqueued: ui4, EnqueueAsNext: Boolean, NumberOfURIs: ui4, EnqueuedURIsAndMetaData: String) -> (FirstTrackNumberEnqueued: ui4, NumTracksAdded: ui4, NewQueueLength: ui4, NewUpdateID: ui4)
      AC: AttachQueue(QueueOwnerID: String) -> (QueueID: ui4, QueueOwnerContext: String)
      AC: Backup()
      AC: Browse(QueueID: ui4, StartingIndex: ui4, RequestedCount: ui4) -> (Result: String, NumberReturned: ui4, TotalMatches: ui4, UpdateID: ui4)
      AC: CreateQueue(QueueOwnerID: String, QueueOwnerContext: String, QueuePolicy: String) -> (QueueID: ui4)
      AC: RemoveAllTracks(QueueID: ui4, UpdateID: ui4) -> (NewUpdateID: ui4)
      AC: RemoveTrackRange(QueueID: ui4, UpdateID: ui4, StartingIndex: ui4, NumberOfTracks: ui4) -> (NewUpdateID: ui4)
      AC: ReorderTracks(QueueID: ui4, StartingIndex: ui4, NumberOfTracks: ui4, InsertBefore: ui4, UpdateID: ui4) -> (NewUpdateID: ui4)
      AC: ReplaceAllTracks(QueueID: ui4, UpdateID: ui4, ContainerURI: String, ContainerMetaData: String, CurrentTrackIndex: ui4, NewCurrentTrackIndices: String, NumberOfURIs: ui4, EnqueuedURIsAndMetaData: String) -> (NewQueueLength: ui4, NewUpdateID: ui4)
      AC: SaveAsSonosPlaylist(QueueID: ui4, Title: String, ObjectID: String) -> (AssignedObjectID: String)
   - urn:schemas-upnp-org:service:GroupRenderingControl:1
      SV: GroupMute
      SV: GroupVolume
      SV: GroupVolumeChangeable
      SV: A_ARG_TYPE_InstanceID
      SV: A_ARG_TYPE_VolumeAdjustment
      AC: GetGroupMute(InstanceID: ui4) -> (CurrentMute: Boolean)
      AC: SetGroupMute(InstanceID: ui4, DesiredMute: Boolean)
      AC: GetGroupVolume(InstanceID: ui4) -> (CurrentVolume: ui2)
      AC: SetGroupVolume(InstanceID: ui4, DesiredVolume: ui2)
      AC: SetRelativeGroupVolume(InstanceID: ui4, Adjustment: i4) -> (NewVolume: ui2)
      AC: SnapshotGroupVolume(InstanceID: ui4)
   - urn:schemas-upnp-org:service:VirtualLineIn:1
      SV: A_ARG_TYPE_InstanceID
      SV: A_ARG_TYPE_PlayerID
      SV: A_ARG_TYPE_Volume
      SV: A_ARG_TYPE_CurrentTransportSettings
      SV: A_ARG_TYPE_Speed
      SV: CurrentTrackMetaData
      SV: EnqueuedTransportURIMetaData
      SV: AVTransportURIMetaData
      SV: CurrentTransportActions
      SV: LastChange
      AC: StartTransmission(InstanceID: ui4, CoordinatorID: String) -> (CurrentTransportSettings: String)
      AC: StopTransmission(InstanceID: ui4, CoordinatorID: String)
      AC: Play(InstanceID: ui4, Speed: String)
      AC: Pause(InstanceID: ui4)
      AC: Next(InstanceID: ui4)
      AC: Previous(InstanceID: ui4)
      AC: Stop(InstanceID: ui4)
      AC: SetVolume(InstanceID: ui4, DesiredVolume: ui2)